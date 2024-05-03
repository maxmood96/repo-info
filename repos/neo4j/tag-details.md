<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.33`](#neo4j4433)
-	[`neo4j:4.4.33-community`](#neo4j4433-community)
-	[`neo4j:4.4.33-enterprise`](#neo4j4433-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-community-ubi9`](#neo4j5-community-ubi9)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-enterprise-ubi9`](#neo4j5-enterprise-ubi9)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5-ubi9`](#neo4j5-ubi9)
-	[`neo4j:5.19`](#neo4j519)
-	[`neo4j:5.19-bullseye`](#neo4j519-bullseye)
-	[`neo4j:5.19-community`](#neo4j519-community)
-	[`neo4j:5.19-community-bullseye`](#neo4j519-community-bullseye)
-	[`neo4j:5.19-community-ubi8`](#neo4j519-community-ubi8)
-	[`neo4j:5.19-community-ubi9`](#neo4j519-community-ubi9)
-	[`neo4j:5.19-enterprise`](#neo4j519-enterprise)
-	[`neo4j:5.19-enterprise-bullseye`](#neo4j519-enterprise-bullseye)
-	[`neo4j:5.19-enterprise-ubi8`](#neo4j519-enterprise-ubi8)
-	[`neo4j:5.19-enterprise-ubi9`](#neo4j519-enterprise-ubi9)
-	[`neo4j:5.19-ubi8`](#neo4j519-ubi8)
-	[`neo4j:5.19-ubi9`](#neo4j519-ubi9)
-	[`neo4j:5.19.0`](#neo4j5190)
-	[`neo4j:5.19.0-bullseye`](#neo4j5190-bullseye)
-	[`neo4j:5.19.0-community`](#neo4j5190-community)
-	[`neo4j:5.19.0-community-bullseye`](#neo4j5190-community-bullseye)
-	[`neo4j:5.19.0-community-ubi8`](#neo4j5190-community-ubi8)
-	[`neo4j:5.19.0-community-ubi9`](#neo4j5190-community-ubi9)
-	[`neo4j:5.19.0-enterprise`](#neo4j5190-enterprise)
-	[`neo4j:5.19.0-enterprise-bullseye`](#neo4j5190-enterprise-bullseye)
-	[`neo4j:5.19.0-enterprise-ubi8`](#neo4j5190-enterprise-ubi8)
-	[`neo4j:5.19.0-enterprise-ubi9`](#neo4j5190-enterprise-ubi9)
-	[`neo4j:5.19.0-ubi8`](#neo4j5190-ubi8)
-	[`neo4j:5.19.0-ubi9`](#neo4j5190-ubi9)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi8`](#neo4jcommunity-ubi8)
-	[`neo4j:community-ubi9`](#neo4jcommunity-ubi9)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi8`](#neo4jenterprise-ubi8)
-	[`neo4j:enterprise-ubi9`](#neo4jenterprise-ubi9)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi8`](#neo4jubi8)
-	[`neo4j:ubi9`](#neo4jubi9)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:634389291b2ea4e60eb6d47e56815e41d87ef0eff9963c874c6a812290a5e7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:bf6b38e7826d2b40111c782f23cd955fd9c1c5e2b78aca8f0fddea15e6006037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297972539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4fb4aedf8a27d6507a1044cfb75efdb0f27a556974d8f657161478ef067046`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da1a6e9792f761b30ce0da3c610fc2738d413a33df86dd0d5a274e944bf45fbd NEO4J_TARBALL=neo4j-community-4.4.33-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5b12a1bd5e5b8d801ba2345508c3691ebd68d611a66987294c61803c0a7e47`  
		Last Modified: Thu, 02 May 2024 01:51:28 GMT  
		Size: 145.5 MB (145504895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af55715e2a147880b1289de53b3bf27f3eebef0b53c3bd6a525bf91736408575`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73cac764d4decc7c23bd37afa85a7c93cf8c720cfc66e8d7fda7e4878bebfd6`  
		Last Modified: Thu, 02 May 2024 01:51:27 GMT  
		Size: 121.0 MB (121020066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:a6480cf0a51ad56d6754ed38726e52a6f60def43795d96238eac5c6a86464af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e247e65c2b65cdde804abf3c25920f49cb38346ff527a757ca9850a536c04c6a`

```dockerfile
```

-	Layers:
	-	`sha256:b8e5eb706c64a5c2c88437b357c5c283586733897116972d85857746590aad35`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 2.9 MB (2940185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f86c3e380f2269b25b1293358587767e179b3eaa5e0a94e454ccb905717ee0`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 20.5 KB (20470 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c7fad6dfdbe8d1bc0f8d428d0414c2112bed49f8c6429dd3f759f68dd4345210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293390067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488b25af648c3dc1c162e31e45f9f421e3cbba26f35ecdfa73a66ada9d69e78a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da1a6e9792f761b30ce0da3c610fc2738d413a33df86dd0d5a274e944bf45fbd NEO4J_TARBALL=neo4j-community-4.4.33-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992bdb3a7d4ff5d9d83ff255dcda38aceae1b4e3e7f3638efb4281d8763baf88`  
		Last Modified: Thu, 02 May 2024 12:33:56 GMT  
		Size: 142.3 MB (142304144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a05d2aec54e9a114c3456cb1ead7395dfd05847e98636639836143884b7d3`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6891a86e41c97d70e638162b116eaeca8b8350f63a9e4f61e1cecefa6639d1d`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d33a91dea9d423ab5ff98e92cdf4b6c2426cd3d8bb6df80452b32dcb5debb4`  
		Last Modified: Thu, 02 May 2024 12:33:55 GMT  
		Size: 121.0 MB (120985242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:3e171126b3e1afb833a2f101db726114c59db6aef1af55c60d4f9e5c5e2c3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648168291cba3c8852378674af377de81c855fee4bcd9aac925309fe1aafa33`

```dockerfile
```

-	Layers:
	-	`sha256:57c95ea4ada6f54ede69e64a9ec9fb552ce9c7cc38dac212e914b025888127b5`  
		Last Modified: Thu, 02 May 2024 12:33:53 GMT  
		Size: 2.9 MB (2940403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58716508487ae95cba81773878d7e5f2a5905bc194d381b75dbc7a8e4c5a6df`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 20.3 KB (20315 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:634389291b2ea4e60eb6d47e56815e41d87ef0eff9963c874c6a812290a5e7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:bf6b38e7826d2b40111c782f23cd955fd9c1c5e2b78aca8f0fddea15e6006037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297972539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4fb4aedf8a27d6507a1044cfb75efdb0f27a556974d8f657161478ef067046`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da1a6e9792f761b30ce0da3c610fc2738d413a33df86dd0d5a274e944bf45fbd NEO4J_TARBALL=neo4j-community-4.4.33-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5b12a1bd5e5b8d801ba2345508c3691ebd68d611a66987294c61803c0a7e47`  
		Last Modified: Thu, 02 May 2024 01:51:28 GMT  
		Size: 145.5 MB (145504895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af55715e2a147880b1289de53b3bf27f3eebef0b53c3bd6a525bf91736408575`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73cac764d4decc7c23bd37afa85a7c93cf8c720cfc66e8d7fda7e4878bebfd6`  
		Last Modified: Thu, 02 May 2024 01:51:27 GMT  
		Size: 121.0 MB (121020066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a6480cf0a51ad56d6754ed38726e52a6f60def43795d96238eac5c6a86464af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e247e65c2b65cdde804abf3c25920f49cb38346ff527a757ca9850a536c04c6a`

```dockerfile
```

-	Layers:
	-	`sha256:b8e5eb706c64a5c2c88437b357c5c283586733897116972d85857746590aad35`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 2.9 MB (2940185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f86c3e380f2269b25b1293358587767e179b3eaa5e0a94e454ccb905717ee0`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 20.5 KB (20470 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c7fad6dfdbe8d1bc0f8d428d0414c2112bed49f8c6429dd3f759f68dd4345210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293390067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488b25af648c3dc1c162e31e45f9f421e3cbba26f35ecdfa73a66ada9d69e78a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da1a6e9792f761b30ce0da3c610fc2738d413a33df86dd0d5a274e944bf45fbd NEO4J_TARBALL=neo4j-community-4.4.33-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992bdb3a7d4ff5d9d83ff255dcda38aceae1b4e3e7f3638efb4281d8763baf88`  
		Last Modified: Thu, 02 May 2024 12:33:56 GMT  
		Size: 142.3 MB (142304144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a05d2aec54e9a114c3456cb1ead7395dfd05847e98636639836143884b7d3`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6891a86e41c97d70e638162b116eaeca8b8350f63a9e4f61e1cecefa6639d1d`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d33a91dea9d423ab5ff98e92cdf4b6c2426cd3d8bb6df80452b32dcb5debb4`  
		Last Modified: Thu, 02 May 2024 12:33:55 GMT  
		Size: 121.0 MB (120985242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:3e171126b3e1afb833a2f101db726114c59db6aef1af55c60d4f9e5c5e2c3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648168291cba3c8852378674af377de81c855fee4bcd9aac925309fe1aafa33`

```dockerfile
```

-	Layers:
	-	`sha256:57c95ea4ada6f54ede69e64a9ec9fb552ce9c7cc38dac212e914b025888127b5`  
		Last Modified: Thu, 02 May 2024 12:33:53 GMT  
		Size: 2.9 MB (2940403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58716508487ae95cba81773878d7e5f2a5905bc194d381b75dbc7a8e4c5a6df`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 20.3 KB (20315 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:a05639c897fb6053195a2adb7b1f8ac17f13bc358f02997ec28cb3e81d7e5a36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2d8eb4687eed5a386b6a6b1a9467b5c3c326e6e5a631269f5ba1f66927f551e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402701177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e9ecd64aa578523d3455cc69763ca0709833b80f1d0401ca2b6890cb48a481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1435cf0d7b8d46a3c63e791ea3af75ff904671de8bd68a4941c4a282f8b39418 NEO4J_TARBALL=neo4j-enterprise-4.4.33-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5b12a1bd5e5b8d801ba2345508c3691ebd68d611a66987294c61803c0a7e47`  
		Last Modified: Thu, 02 May 2024 01:51:28 GMT  
		Size: 145.5 MB (145504895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620639c5c1058a83d3d92dfeba565630ef0d6c904fcf6a1ecb37e8c12eb7b4d4`  
		Last Modified: Thu, 02 May 2024 01:51:30 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929007eb7f5e2e37b05511e7eecd7b7ba33e946dc77790abcedd5498a24d7ddc`  
		Last Modified: Thu, 02 May 2024 01:51:30 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9d669b9348fc62273bd6c246e86775f673f1022abda40fcf1e41833bc5719`  
		Last Modified: Thu, 02 May 2024 01:51:33 GMT  
		Size: 225.7 MB (225748700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b093db064319c80d0c9e865b84d8ddcca7a277528221a078aa539bd2a1a984cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae022b37656ef3efa34d0c2dccaf9622ae1662c3be83a2dedefd077c38afed6`

```dockerfile
```

-	Layers:
	-	`sha256:c2a213ff3723dc0d7bc4d026f359820183fa567e33bde3a407eaacc0670daf36`  
		Last Modified: Thu, 02 May 2024 01:51:30 GMT  
		Size: 3.1 MB (3069495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ad7f2f869840fa14294cbc484529ea7f3130968684b83abafce1a6b608c04b`  
		Last Modified: Thu, 02 May 2024 01:51:30 GMT  
		Size: 19.9 KB (19903 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:98376d03b80b0ab8e2cb7423cf41e15524ce945fea9d956b2a2d15f25eab408c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.1 MB (398117070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee92764f94a1c5981caa274dad6fc0767dcc9993a3e6c645332e71fe08f1739e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1435cf0d7b8d46a3c63e791ea3af75ff904671de8bd68a4941c4a282f8b39418 NEO4J_TARBALL=neo4j-enterprise-4.4.33-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992bdb3a7d4ff5d9d83ff255dcda38aceae1b4e3e7f3638efb4281d8763baf88`  
		Last Modified: Thu, 02 May 2024 12:33:56 GMT  
		Size: 142.3 MB (142304144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5186ae673a569e7bb2ed50228af2b2d425b37ff428bc8ae9978ede56dd7d2100`  
		Last Modified: Thu, 02 May 2024 12:34:53 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb850a5cbed270ed54a553ac5ec151afb267d00798c01c9575f876e7d1091654`  
		Last Modified: Thu, 02 May 2024 12:34:53 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab1564c05d789ca984663870ecc9fbeca5166ec82c0e9632d27b75c3b5e53e`  
		Last Modified: Thu, 02 May 2024 12:34:59 GMT  
		Size: 225.7 MB (225712245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:893a75cbb452f9a15f13d527c453b713859b882b1c6a13ba1995dee373e39034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70910616d5d0aa8647ad212952370e35cf057d9dca2089c99dd95d7985c5606`

```dockerfile
```

-	Layers:
	-	`sha256:8a4a2e7c1369ae1711d22fe551754342fa50b6295912b764aad3704f2f2f5b38`  
		Last Modified: Thu, 02 May 2024 12:34:53 GMT  
		Size: 3.1 MB (3069709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78142cee93b84aec0c61c41501a0a6eb28c1abb26aa3334b9428d7d527c4e01`  
		Last Modified: Thu, 02 May 2024 12:34:53 GMT  
		Size: 18.9 KB (18924 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.33`

```console
$ docker pull neo4j@sha256:634389291b2ea4e60eb6d47e56815e41d87ef0eff9963c874c6a812290a5e7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.33` - linux; amd64

```console
$ docker pull neo4j@sha256:bf6b38e7826d2b40111c782f23cd955fd9c1c5e2b78aca8f0fddea15e6006037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297972539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4fb4aedf8a27d6507a1044cfb75efdb0f27a556974d8f657161478ef067046`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da1a6e9792f761b30ce0da3c610fc2738d413a33df86dd0d5a274e944bf45fbd NEO4J_TARBALL=neo4j-community-4.4.33-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5b12a1bd5e5b8d801ba2345508c3691ebd68d611a66987294c61803c0a7e47`  
		Last Modified: Thu, 02 May 2024 01:51:28 GMT  
		Size: 145.5 MB (145504895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af55715e2a147880b1289de53b3bf27f3eebef0b53c3bd6a525bf91736408575`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73cac764d4decc7c23bd37afa85a7c93cf8c720cfc66e8d7fda7e4878bebfd6`  
		Last Modified: Thu, 02 May 2024 01:51:27 GMT  
		Size: 121.0 MB (121020066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33` - unknown; unknown

```console
$ docker pull neo4j@sha256:a6480cf0a51ad56d6754ed38726e52a6f60def43795d96238eac5c6a86464af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e247e65c2b65cdde804abf3c25920f49cb38346ff527a757ca9850a536c04c6a`

```dockerfile
```

-	Layers:
	-	`sha256:b8e5eb706c64a5c2c88437b357c5c283586733897116972d85857746590aad35`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 2.9 MB (2940185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f86c3e380f2269b25b1293358587767e179b3eaa5e0a94e454ccb905717ee0`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 20.5 KB (20470 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.33` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c7fad6dfdbe8d1bc0f8d428d0414c2112bed49f8c6429dd3f759f68dd4345210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293390067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488b25af648c3dc1c162e31e45f9f421e3cbba26f35ecdfa73a66ada9d69e78a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da1a6e9792f761b30ce0da3c610fc2738d413a33df86dd0d5a274e944bf45fbd NEO4J_TARBALL=neo4j-community-4.4.33-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992bdb3a7d4ff5d9d83ff255dcda38aceae1b4e3e7f3638efb4281d8763baf88`  
		Last Modified: Thu, 02 May 2024 12:33:56 GMT  
		Size: 142.3 MB (142304144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a05d2aec54e9a114c3456cb1ead7395dfd05847e98636639836143884b7d3`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6891a86e41c97d70e638162b116eaeca8b8350f63a9e4f61e1cecefa6639d1d`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d33a91dea9d423ab5ff98e92cdf4b6c2426cd3d8bb6df80452b32dcb5debb4`  
		Last Modified: Thu, 02 May 2024 12:33:55 GMT  
		Size: 121.0 MB (120985242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33` - unknown; unknown

```console
$ docker pull neo4j@sha256:3e171126b3e1afb833a2f101db726114c59db6aef1af55c60d4f9e5c5e2c3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648168291cba3c8852378674af377de81c855fee4bcd9aac925309fe1aafa33`

```dockerfile
```

-	Layers:
	-	`sha256:57c95ea4ada6f54ede69e64a9ec9fb552ce9c7cc38dac212e914b025888127b5`  
		Last Modified: Thu, 02 May 2024 12:33:53 GMT  
		Size: 2.9 MB (2940403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58716508487ae95cba81773878d7e5f2a5905bc194d381b75dbc7a8e4c5a6df`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 20.3 KB (20315 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.33-community`

```console
$ docker pull neo4j@sha256:634389291b2ea4e60eb6d47e56815e41d87ef0eff9963c874c6a812290a5e7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.33-community` - linux; amd64

```console
$ docker pull neo4j@sha256:bf6b38e7826d2b40111c782f23cd955fd9c1c5e2b78aca8f0fddea15e6006037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297972539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4fb4aedf8a27d6507a1044cfb75efdb0f27a556974d8f657161478ef067046`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da1a6e9792f761b30ce0da3c610fc2738d413a33df86dd0d5a274e944bf45fbd NEO4J_TARBALL=neo4j-community-4.4.33-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5b12a1bd5e5b8d801ba2345508c3691ebd68d611a66987294c61803c0a7e47`  
		Last Modified: Thu, 02 May 2024 01:51:28 GMT  
		Size: 145.5 MB (145504895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af55715e2a147880b1289de53b3bf27f3eebef0b53c3bd6a525bf91736408575`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73cac764d4decc7c23bd37afa85a7c93cf8c720cfc66e8d7fda7e4878bebfd6`  
		Last Modified: Thu, 02 May 2024 01:51:27 GMT  
		Size: 121.0 MB (121020066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a6480cf0a51ad56d6754ed38726e52a6f60def43795d96238eac5c6a86464af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e247e65c2b65cdde804abf3c25920f49cb38346ff527a757ca9850a536c04c6a`

```dockerfile
```

-	Layers:
	-	`sha256:b8e5eb706c64a5c2c88437b357c5c283586733897116972d85857746590aad35`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 2.9 MB (2940185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f86c3e380f2269b25b1293358587767e179b3eaa5e0a94e454ccb905717ee0`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 20.5 KB (20470 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.33-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c7fad6dfdbe8d1bc0f8d428d0414c2112bed49f8c6429dd3f759f68dd4345210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293390067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488b25af648c3dc1c162e31e45f9f421e3cbba26f35ecdfa73a66ada9d69e78a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da1a6e9792f761b30ce0da3c610fc2738d413a33df86dd0d5a274e944bf45fbd NEO4J_TARBALL=neo4j-community-4.4.33-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992bdb3a7d4ff5d9d83ff255dcda38aceae1b4e3e7f3638efb4281d8763baf88`  
		Last Modified: Thu, 02 May 2024 12:33:56 GMT  
		Size: 142.3 MB (142304144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a05d2aec54e9a114c3456cb1ead7395dfd05847e98636639836143884b7d3`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6891a86e41c97d70e638162b116eaeca8b8350f63a9e4f61e1cecefa6639d1d`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d33a91dea9d423ab5ff98e92cdf4b6c2426cd3d8bb6df80452b32dcb5debb4`  
		Last Modified: Thu, 02 May 2024 12:33:55 GMT  
		Size: 121.0 MB (120985242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:3e171126b3e1afb833a2f101db726114c59db6aef1af55c60d4f9e5c5e2c3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648168291cba3c8852378674af377de81c855fee4bcd9aac925309fe1aafa33`

```dockerfile
```

-	Layers:
	-	`sha256:57c95ea4ada6f54ede69e64a9ec9fb552ce9c7cc38dac212e914b025888127b5`  
		Last Modified: Thu, 02 May 2024 12:33:53 GMT  
		Size: 2.9 MB (2940403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58716508487ae95cba81773878d7e5f2a5905bc194d381b75dbc7a8e4c5a6df`  
		Last Modified: Thu, 02 May 2024 12:33:52 GMT  
		Size: 20.3 KB (20315 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.33-enterprise`

```console
$ docker pull neo4j@sha256:a05639c897fb6053195a2adb7b1f8ac17f13bc358f02997ec28cb3e81d7e5a36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.33-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2d8eb4687eed5a386b6a6b1a9467b5c3c326e6e5a631269f5ba1f66927f551e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402701177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e9ecd64aa578523d3455cc69763ca0709833b80f1d0401ca2b6890cb48a481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1435cf0d7b8d46a3c63e791ea3af75ff904671de8bd68a4941c4a282f8b39418 NEO4J_TARBALL=neo4j-enterprise-4.4.33-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5b12a1bd5e5b8d801ba2345508c3691ebd68d611a66987294c61803c0a7e47`  
		Last Modified: Thu, 02 May 2024 01:51:28 GMT  
		Size: 145.5 MB (145504895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620639c5c1058a83d3d92dfeba565630ef0d6c904fcf6a1ecb37e8c12eb7b4d4`  
		Last Modified: Thu, 02 May 2024 01:51:30 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929007eb7f5e2e37b05511e7eecd7b7ba33e946dc77790abcedd5498a24d7ddc`  
		Last Modified: Thu, 02 May 2024 01:51:30 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9d669b9348fc62273bd6c246e86775f673f1022abda40fcf1e41833bc5719`  
		Last Modified: Thu, 02 May 2024 01:51:33 GMT  
		Size: 225.7 MB (225748700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b093db064319c80d0c9e865b84d8ddcca7a277528221a078aa539bd2a1a984cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae022b37656ef3efa34d0c2dccaf9622ae1662c3be83a2dedefd077c38afed6`

```dockerfile
```

-	Layers:
	-	`sha256:c2a213ff3723dc0d7bc4d026f359820183fa567e33bde3a407eaacc0670daf36`  
		Last Modified: Thu, 02 May 2024 01:51:30 GMT  
		Size: 3.1 MB (3069495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ad7f2f869840fa14294cbc484529ea7f3130968684b83abafce1a6b608c04b`  
		Last Modified: Thu, 02 May 2024 01:51:30 GMT  
		Size: 19.9 KB (19903 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.33-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:98376d03b80b0ab8e2cb7423cf41e15524ce945fea9d956b2a2d15f25eab408c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.1 MB (398117070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee92764f94a1c5981caa274dad6fc0767dcc9993a3e6c645332e71fe08f1739e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 09:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1435cf0d7b8d46a3c63e791ea3af75ff904671de8bd68a4941c4a282f8b39418 NEO4J_TARBALL=neo4j-enterprise-4.4.33-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.33-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Apr 2024 09:36:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 09:36:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Apr 2024 09:36:34 GMT
VOLUME [/data /logs]
# Wed, 24 Apr 2024 09:36:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Apr 2024 09:36:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:36:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992bdb3a7d4ff5d9d83ff255dcda38aceae1b4e3e7f3638efb4281d8763baf88`  
		Last Modified: Thu, 02 May 2024 12:33:56 GMT  
		Size: 142.3 MB (142304144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5186ae673a569e7bb2ed50228af2b2d425b37ff428bc8ae9978ede56dd7d2100`  
		Last Modified: Thu, 02 May 2024 12:34:53 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb850a5cbed270ed54a553ac5ec151afb267d00798c01c9575f876e7d1091654`  
		Last Modified: Thu, 02 May 2024 12:34:53 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab1564c05d789ca984663870ecc9fbeca5166ec82c0e9632d27b75c3b5e53e`  
		Last Modified: Thu, 02 May 2024 12:34:59 GMT  
		Size: 225.7 MB (225712245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:893a75cbb452f9a15f13d527c453b713859b882b1c6a13ba1995dee373e39034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70910616d5d0aa8647ad212952370e35cf057d9dca2089c99dd95d7985c5606`

```dockerfile
```

-	Layers:
	-	`sha256:8a4a2e7c1369ae1711d22fe551754342fa50b6295912b764aad3704f2f2f5b38`  
		Last Modified: Thu, 02 May 2024 12:34:53 GMT  
		Size: 3.1 MB (3069709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78142cee93b84aec0c61c41501a0a6eb28c1abb26aa3334b9428d7d527c4e01`  
		Last Modified: Thu, 02 May 2024 12:34:53 GMT  
		Size: 18.9 KB (18924 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:0370858e78423be0df5631d3e15a9240fdb4f35c42990463f539aa2a481ce46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:2a6ab281aa79fec880ea0e862ee98b67102bd7d212a58192bf6e6fe9b850cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287447087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe745bce68aedcc89238cc1a54d2d36f3b975c1f6819fc9278cda1a3064c2b07`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff05d8cb69b295f1af1e76641afb4691e2b93717cc840209cc62b290660ce9`  
		Last Modified: Thu, 02 May 2024 23:53:09 GMT  
		Size: 125.7 MB (125724994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d428b6aac31517b14c31ad9a634a823c6bba17c66952e5e54e3bf678c5c06c`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad504d95aab247d56384379e3edd2738684943318c763509723ce7e7680c83e0`  
		Last Modified: Thu, 02 May 2024 23:53:08 GMT  
		Size: 122.8 MB (122827043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2edcd2b61e533ecce8fb6ff0414237cbfd2676db105a642b7d7bba5b5c072e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb465354dffe507ece70f10f36380ab315b0e9b14ec9dc67ddc71261e9a78d7`

```dockerfile
```

-	Layers:
	-	`sha256:ddf95c3c44a1aecdf0844d99c9fd06c3c5ff1f32f054478d0bcc1c7d6b54c8d5`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8869c27f54df932f01dbb439c3cf9b6c1b441875aea1af33dcfc6937531bd`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7305b5dd392fb2af49bf1c34bdf80b2e4eea03ac4a3536eb57cdffa736d43b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285708915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c352a0746c8292b35ea8fb2dccc007ee013a355d9efb72e5b80dadffb13f115b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f5f71f9a33e678f6bb048d024e0f49df09d3969eab9252357da8132a3ed`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 122.8 MB (122827013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e7dfe92615851220bfc32bc73235b75a14ff18fa815979efc8d28f9c5626ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f5f903abc3abea14bc8d514c7cb77828d1f4d88873b8286405b57ee8b9908`

```dockerfile
```

-	Layers:
	-	`sha256:594b8f5fd581daf798dcb8933a5ed92b8a225c68583feb07384e1dafc83a6c3f`  
		Last Modified: Fri, 03 May 2024 01:53:06 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070b1734dd9ff6e261e929866fbea0f41e7750384b3f087d69b593e0f76301e`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:4dcb01cbb1fd8c3d43592557d904068e0f912c102685863bdcc921625aff6e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:52e88b3d625dac9f6c5ae4420534dbb4df6000c0df097232d34e17676e0a62a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59da8fc4fdd58b2d9c2b4ff053a53219b0835d3f0e28390cbc36ac7f56b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb644f90a595a86ac6a3d87c40742d500e6843f922e6d21e8fd8992aa881ba5d`  
		Last Modified: Thu, 02 May 2024 01:51:52 GMT  
		Size: 145.1 MB (145095087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa30e0bc3f6c2ccfdf0951cee89e2b0593d106ded99ebbd8c12cc7663c130ac`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873a66af9faccde7bfd9293d66333f2cdfc34fe0bc05e0232eacb211d48983f`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26209796074bd6bc871da2c60e1872c271baddbddf8d913759ec003da80b4c61`  
		Last Modified: Thu, 02 May 2024 01:51:55 GMT  
		Size: 384.2 MB (384218824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e49bbd140e7db653fb626e909a5ee719a50587557a9c7a9bfdcd8ae54d5f801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf7a4e6d79ae6ac9a83931e855e6a98691cc81b7c92b96c014a50796797fbc`

```dockerfile
```

-	Layers:
	-	`sha256:32dd6421b7e506a5f4213a62dedb3593dccf9d3db2460dba8d93c56bbd198d35`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.1 MB (3127644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61543321fd341dbb90794a30fe6c0c8c8d9be9e3db99c09dac3a6f48ff5dd6b`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

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

### `neo4j:5-enterprise` - unknown; unknown

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

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4dcb01cbb1fd8c3d43592557d904068e0f912c102685863bdcc921625aff6e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:52e88b3d625dac9f6c5ae4420534dbb4df6000c0df097232d34e17676e0a62a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59da8fc4fdd58b2d9c2b4ff053a53219b0835d3f0e28390cbc36ac7f56b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb644f90a595a86ac6a3d87c40742d500e6843f922e6d21e8fd8992aa881ba5d`  
		Last Modified: Thu, 02 May 2024 01:51:52 GMT  
		Size: 145.1 MB (145095087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa30e0bc3f6c2ccfdf0951cee89e2b0593d106ded99ebbd8c12cc7663c130ac`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873a66af9faccde7bfd9293d66333f2cdfc34fe0bc05e0232eacb211d48983f`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26209796074bd6bc871da2c60e1872c271baddbddf8d913759ec003da80b4c61`  
		Last Modified: Thu, 02 May 2024 01:51:55 GMT  
		Size: 384.2 MB (384218824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e49bbd140e7db653fb626e909a5ee719a50587557a9c7a9bfdcd8ae54d5f801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf7a4e6d79ae6ac9a83931e855e6a98691cc81b7c92b96c014a50796797fbc`

```dockerfile
```

-	Layers:
	-	`sha256:32dd6421b7e506a5f4213a62dedb3593dccf9d3db2460dba8d93c56bbd198d35`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.1 MB (3127644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61543321fd341dbb90794a30fe6c0c8c8d9be9e3db99c09dac3a6f48ff5dd6b`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

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

### `neo4j:5-enterprise-bullseye` - unknown; unknown

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

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4b46fa568dd07658aa91edb82a39cd6ab1da29594e85f0e64a7b6b34852cdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:27147d063acb685ad1fa5ff0f3a8830474951d837c10dc25d12c686a96c0d07c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:17aae81547e1f67437f422bbe8b4905143a7ee0130addebe0a5f9af4d4c0fabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545903582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ae3416e60e7423ed433a1975976791ac0afa84938c3c7ec8ebc24cc155212`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779ab28fbb304705ac05e7124f76e128ac2b417e433def98b2e03a28a308cea8`  
		Last Modified: Thu, 02 May 2024 23:53:01 GMT  
		Size: 125.7 MB (125724901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ad1a153a6a805f6b821110ff771e59cabedcce497121a9a83973c0666561d5`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2224f4f7fb46927c2ed3be5d3cdf8eed6d022dfb815480eec737ac4c1f2d`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 381.3 MB (381283629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5cf351076202fa7c397d8c19e02c3365d655080504bdfc54d74bfe53cc2c462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e131ec1c4e1df19bac37b93cf6535326f7c0ad15c7dcb95d3a4861859914ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:e8a7df93cf7344a2ca85dc52ba52955082fd0add9b94f3b7d2502e8703e2f254`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 5.6 MB (5596528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f149ddd3a2723a5e89cc68e33c6012f5a23df12df780b5f0d1109b5d964b1a10`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 20.5 KB (20487 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13ab96e07f5567a7dfe1100c550f5b9b66864ffd205a3aedf9f11e9e59a99283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.2 MB (544165548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f842f62f69ce0ae41172018a2e6b2c8db7374e49fa38f93e780c1d766912084`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c25209986e4a6b63e445440325ed351ffe62ba63f57b21bd1a5613db5f2046`  
		Last Modified: Fri, 03 May 2024 02:17:13 GMT  
		Size: 381.3 MB (381283646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c16bad0ddae11ed55105766602ae734f27c06968bd5a2b9453372fd4b2ebed42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5589831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e757531780f5d911f441c92cad7c2f487c14d6ce80f602efcbbacde450816d4`

```dockerfile
```

-	Layers:
	-	`sha256:e7d8614de5e7ffd06d00b3824b584b3e3a2f007cf7008b5258c939717f9d9e6d`  
		Last Modified: Fri, 03 May 2024 02:17:05 GMT  
		Size: 5.6 MB (5569500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30df46436cf08a463dad8f67c3aaa509f8e9de361944e584be15209455b466cc`  
		Last Modified: Fri, 03 May 2024 02:17:05 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:0370858e78423be0df5631d3e15a9240fdb4f35c42990463f539aa2a481ce46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:2a6ab281aa79fec880ea0e862ee98b67102bd7d212a58192bf6e6fe9b850cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287447087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe745bce68aedcc89238cc1a54d2d36f3b975c1f6819fc9278cda1a3064c2b07`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff05d8cb69b295f1af1e76641afb4691e2b93717cc840209cc62b290660ce9`  
		Last Modified: Thu, 02 May 2024 23:53:09 GMT  
		Size: 125.7 MB (125724994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d428b6aac31517b14c31ad9a634a823c6bba17c66952e5e54e3bf678c5c06c`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad504d95aab247d56384379e3edd2738684943318c763509723ce7e7680c83e0`  
		Last Modified: Thu, 02 May 2024 23:53:08 GMT  
		Size: 122.8 MB (122827043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2edcd2b61e533ecce8fb6ff0414237cbfd2676db105a642b7d7bba5b5c072e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb465354dffe507ece70f10f36380ab315b0e9b14ec9dc67ddc71261e9a78d7`

```dockerfile
```

-	Layers:
	-	`sha256:ddf95c3c44a1aecdf0844d99c9fd06c3c5ff1f32f054478d0bcc1c7d6b54c8d5`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8869c27f54df932f01dbb439c3cf9b6c1b441875aea1af33dcfc6937531bd`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7305b5dd392fb2af49bf1c34bdf80b2e4eea03ac4a3536eb57cdffa736d43b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285708915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c352a0746c8292b35ea8fb2dccc007ee013a355d9efb72e5b80dadffb13f115b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f5f71f9a33e678f6bb048d024e0f49df09d3969eab9252357da8132a3ed`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 122.8 MB (122827013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e7dfe92615851220bfc32bc73235b75a14ff18fa815979efc8d28f9c5626ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f5f903abc3abea14bc8d514c7cb77828d1f4d88873b8286405b57ee8b9908`

```dockerfile
```

-	Layers:
	-	`sha256:594b8f5fd581daf798dcb8933a5ed92b8a225c68583feb07384e1dafc83a6c3f`  
		Last Modified: Fri, 03 May 2024 01:53:06 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070b1734dd9ff6e261e929866fbea0f41e7750384b3f087d69b593e0f76301e`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-bullseye`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community-bullseye`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community-ubi9`

```console
$ docker pull neo4j@sha256:0370858e78423be0df5631d3e15a9240fdb4f35c42990463f539aa2a481ce46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:2a6ab281aa79fec880ea0e862ee98b67102bd7d212a58192bf6e6fe9b850cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287447087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe745bce68aedcc89238cc1a54d2d36f3b975c1f6819fc9278cda1a3064c2b07`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff05d8cb69b295f1af1e76641afb4691e2b93717cc840209cc62b290660ce9`  
		Last Modified: Thu, 02 May 2024 23:53:09 GMT  
		Size: 125.7 MB (125724994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d428b6aac31517b14c31ad9a634a823c6bba17c66952e5e54e3bf678c5c06c`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad504d95aab247d56384379e3edd2738684943318c763509723ce7e7680c83e0`  
		Last Modified: Thu, 02 May 2024 23:53:08 GMT  
		Size: 122.8 MB (122827043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2edcd2b61e533ecce8fb6ff0414237cbfd2676db105a642b7d7bba5b5c072e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb465354dffe507ece70f10f36380ab315b0e9b14ec9dc67ddc71261e9a78d7`

```dockerfile
```

-	Layers:
	-	`sha256:ddf95c3c44a1aecdf0844d99c9fd06c3c5ff1f32f054478d0bcc1c7d6b54c8d5`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8869c27f54df932f01dbb439c3cf9b6c1b441875aea1af33dcfc6937531bd`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7305b5dd392fb2af49bf1c34bdf80b2e4eea03ac4a3536eb57cdffa736d43b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285708915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c352a0746c8292b35ea8fb2dccc007ee013a355d9efb72e5b80dadffb13f115b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f5f71f9a33e678f6bb048d024e0f49df09d3969eab9252357da8132a3ed`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 122.8 MB (122827013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e7dfe92615851220bfc32bc73235b75a14ff18fa815979efc8d28f9c5626ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f5f903abc3abea14bc8d514c7cb77828d1f4d88873b8286405b57ee8b9908`

```dockerfile
```

-	Layers:
	-	`sha256:594b8f5fd581daf798dcb8933a5ed92b8a225c68583feb07384e1dafc83a6c3f`  
		Last Modified: Fri, 03 May 2024 01:53:06 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070b1734dd9ff6e261e929866fbea0f41e7750384b3f087d69b593e0f76301e`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-enterprise`

```console
$ docker pull neo4j@sha256:4dcb01cbb1fd8c3d43592557d904068e0f912c102685863bdcc921625aff6e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:52e88b3d625dac9f6c5ae4420534dbb4df6000c0df097232d34e17676e0a62a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59da8fc4fdd58b2d9c2b4ff053a53219b0835d3f0e28390cbc36ac7f56b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb644f90a595a86ac6a3d87c40742d500e6843f922e6d21e8fd8992aa881ba5d`  
		Last Modified: Thu, 02 May 2024 01:51:52 GMT  
		Size: 145.1 MB (145095087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa30e0bc3f6c2ccfdf0951cee89e2b0593d106ded99ebbd8c12cc7663c130ac`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873a66af9faccde7bfd9293d66333f2cdfc34fe0bc05e0232eacb211d48983f`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26209796074bd6bc871da2c60e1872c271baddbddf8d913759ec003da80b4c61`  
		Last Modified: Thu, 02 May 2024 01:51:55 GMT  
		Size: 384.2 MB (384218824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e49bbd140e7db653fb626e909a5ee719a50587557a9c7a9bfdcd8ae54d5f801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf7a4e6d79ae6ac9a83931e855e6a98691cc81b7c92b96c014a50796797fbc`

```dockerfile
```

-	Layers:
	-	`sha256:32dd6421b7e506a5f4213a62dedb3593dccf9d3db2460dba8d93c56bbd198d35`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.1 MB (3127644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61543321fd341dbb90794a30fe6c0c8c8d9be9e3db99c09dac3a6f48ff5dd6b`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise` - linux; arm64 variant v8

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

### `neo4j:5.19-enterprise` - unknown; unknown

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

## `neo4j:5.19-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4dcb01cbb1fd8c3d43592557d904068e0f912c102685863bdcc921625aff6e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:52e88b3d625dac9f6c5ae4420534dbb4df6000c0df097232d34e17676e0a62a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59da8fc4fdd58b2d9c2b4ff053a53219b0835d3f0e28390cbc36ac7f56b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb644f90a595a86ac6a3d87c40742d500e6843f922e6d21e8fd8992aa881ba5d`  
		Last Modified: Thu, 02 May 2024 01:51:52 GMT  
		Size: 145.1 MB (145095087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa30e0bc3f6c2ccfdf0951cee89e2b0593d106ded99ebbd8c12cc7663c130ac`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873a66af9faccde7bfd9293d66333f2cdfc34fe0bc05e0232eacb211d48983f`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26209796074bd6bc871da2c60e1872c271baddbddf8d913759ec003da80b4c61`  
		Last Modified: Thu, 02 May 2024 01:51:55 GMT  
		Size: 384.2 MB (384218824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e49bbd140e7db653fb626e909a5ee719a50587557a9c7a9bfdcd8ae54d5f801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf7a4e6d79ae6ac9a83931e855e6a98691cc81b7c92b96c014a50796797fbc`

```dockerfile
```

-	Layers:
	-	`sha256:32dd6421b7e506a5f4213a62dedb3593dccf9d3db2460dba8d93c56bbd198d35`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.1 MB (3127644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61543321fd341dbb90794a30fe6c0c8c8d9be9e3db99c09dac3a6f48ff5dd6b`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise-bullseye` - linux; arm64 variant v8

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

### `neo4j:5.19-enterprise-bullseye` - unknown; unknown

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

## `neo4j:5.19-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4b46fa568dd07658aa91edb82a39cd6ab1da29594e85f0e64a7b6b34852cdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:27147d063acb685ad1fa5ff0f3a8830474951d837c10dc25d12c686a96c0d07c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:17aae81547e1f67437f422bbe8b4905143a7ee0130addebe0a5f9af4d4c0fabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545903582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ae3416e60e7423ed433a1975976791ac0afa84938c3c7ec8ebc24cc155212`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779ab28fbb304705ac05e7124f76e128ac2b417e433def98b2e03a28a308cea8`  
		Last Modified: Thu, 02 May 2024 23:53:01 GMT  
		Size: 125.7 MB (125724901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ad1a153a6a805f6b821110ff771e59cabedcce497121a9a83973c0666561d5`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2224f4f7fb46927c2ed3be5d3cdf8eed6d022dfb815480eec737ac4c1f2d`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 381.3 MB (381283629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5cf351076202fa7c397d8c19e02c3365d655080504bdfc54d74bfe53cc2c462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e131ec1c4e1df19bac37b93cf6535326f7c0ad15c7dcb95d3a4861859914ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:e8a7df93cf7344a2ca85dc52ba52955082fd0add9b94f3b7d2502e8703e2f254`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 5.6 MB (5596528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f149ddd3a2723a5e89cc68e33c6012f5a23df12df780b5f0d1109b5d964b1a10`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 20.5 KB (20487 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13ab96e07f5567a7dfe1100c550f5b9b66864ffd205a3aedf9f11e9e59a99283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.2 MB (544165548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f842f62f69ce0ae41172018a2e6b2c8db7374e49fa38f93e780c1d766912084`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c25209986e4a6b63e445440325ed351ffe62ba63f57b21bd1a5613db5f2046`  
		Last Modified: Fri, 03 May 2024 02:17:13 GMT  
		Size: 381.3 MB (381283646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c16bad0ddae11ed55105766602ae734f27c06968bd5a2b9453372fd4b2ebed42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5589831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e757531780f5d911f441c92cad7c2f487c14d6ce80f602efcbbacde450816d4`

```dockerfile
```

-	Layers:
	-	`sha256:e7d8614de5e7ffd06d00b3824b584b3e3a2f007cf7008b5258c939717f9d9e6d`  
		Last Modified: Fri, 03 May 2024 02:17:05 GMT  
		Size: 5.6 MB (5569500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30df46436cf08a463dad8f67c3aaa509f8e9de361944e584be15209455b466cc`  
		Last Modified: Fri, 03 May 2024 02:17:05 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-ubi9`

```console
$ docker pull neo4j@sha256:0370858e78423be0df5631d3e15a9240fdb4f35c42990463f539aa2a481ce46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:2a6ab281aa79fec880ea0e862ee98b67102bd7d212a58192bf6e6fe9b850cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287447087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe745bce68aedcc89238cc1a54d2d36f3b975c1f6819fc9278cda1a3064c2b07`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff05d8cb69b295f1af1e76641afb4691e2b93717cc840209cc62b290660ce9`  
		Last Modified: Thu, 02 May 2024 23:53:09 GMT  
		Size: 125.7 MB (125724994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d428b6aac31517b14c31ad9a634a823c6bba17c66952e5e54e3bf678c5c06c`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad504d95aab247d56384379e3edd2738684943318c763509723ce7e7680c83e0`  
		Last Modified: Thu, 02 May 2024 23:53:08 GMT  
		Size: 122.8 MB (122827043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2edcd2b61e533ecce8fb6ff0414237cbfd2676db105a642b7d7bba5b5c072e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb465354dffe507ece70f10f36380ab315b0e9b14ec9dc67ddc71261e9a78d7`

```dockerfile
```

-	Layers:
	-	`sha256:ddf95c3c44a1aecdf0844d99c9fd06c3c5ff1f32f054478d0bcc1c7d6b54c8d5`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8869c27f54df932f01dbb439c3cf9b6c1b441875aea1af33dcfc6937531bd`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7305b5dd392fb2af49bf1c34bdf80b2e4eea03ac4a3536eb57cdffa736d43b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285708915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c352a0746c8292b35ea8fb2dccc007ee013a355d9efb72e5b80dadffb13f115b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f5f71f9a33e678f6bb048d024e0f49df09d3969eab9252357da8132a3ed`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 122.8 MB (122827013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e7dfe92615851220bfc32bc73235b75a14ff18fa815979efc8d28f9c5626ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f5f903abc3abea14bc8d514c7cb77828d1f4d88873b8286405b57ee8b9908`

```dockerfile
```

-	Layers:
	-	`sha256:594b8f5fd581daf798dcb8933a5ed92b8a225c68583feb07384e1dafc83a6c3f`  
		Last Modified: Fri, 03 May 2024 01:53:06 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070b1734dd9ff6e261e929866fbea0f41e7750384b3f087d69b593e0f76301e`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-bullseye`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community-bullseye`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community-ubi9`

```console
$ docker pull neo4j@sha256:0370858e78423be0df5631d3e15a9240fdb4f35c42990463f539aa2a481ce46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:2a6ab281aa79fec880ea0e862ee98b67102bd7d212a58192bf6e6fe9b850cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287447087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe745bce68aedcc89238cc1a54d2d36f3b975c1f6819fc9278cda1a3064c2b07`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff05d8cb69b295f1af1e76641afb4691e2b93717cc840209cc62b290660ce9`  
		Last Modified: Thu, 02 May 2024 23:53:09 GMT  
		Size: 125.7 MB (125724994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d428b6aac31517b14c31ad9a634a823c6bba17c66952e5e54e3bf678c5c06c`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad504d95aab247d56384379e3edd2738684943318c763509723ce7e7680c83e0`  
		Last Modified: Thu, 02 May 2024 23:53:08 GMT  
		Size: 122.8 MB (122827043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2edcd2b61e533ecce8fb6ff0414237cbfd2676db105a642b7d7bba5b5c072e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb465354dffe507ece70f10f36380ab315b0e9b14ec9dc67ddc71261e9a78d7`

```dockerfile
```

-	Layers:
	-	`sha256:ddf95c3c44a1aecdf0844d99c9fd06c3c5ff1f32f054478d0bcc1c7d6b54c8d5`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8869c27f54df932f01dbb439c3cf9b6c1b441875aea1af33dcfc6937531bd`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7305b5dd392fb2af49bf1c34bdf80b2e4eea03ac4a3536eb57cdffa736d43b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285708915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c352a0746c8292b35ea8fb2dccc007ee013a355d9efb72e5b80dadffb13f115b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f5f71f9a33e678f6bb048d024e0f49df09d3969eab9252357da8132a3ed`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 122.8 MB (122827013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e7dfe92615851220bfc32bc73235b75a14ff18fa815979efc8d28f9c5626ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f5f903abc3abea14bc8d514c7cb77828d1f4d88873b8286405b57ee8b9908`

```dockerfile
```

-	Layers:
	-	`sha256:594b8f5fd581daf798dcb8933a5ed92b8a225c68583feb07384e1dafc83a6c3f`  
		Last Modified: Fri, 03 May 2024 01:53:06 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070b1734dd9ff6e261e929866fbea0f41e7750384b3f087d69b593e0f76301e`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-enterprise`

```console
$ docker pull neo4j@sha256:4dcb01cbb1fd8c3d43592557d904068e0f912c102685863bdcc921625aff6e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:52e88b3d625dac9f6c5ae4420534dbb4df6000c0df097232d34e17676e0a62a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59da8fc4fdd58b2d9c2b4ff053a53219b0835d3f0e28390cbc36ac7f56b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb644f90a595a86ac6a3d87c40742d500e6843f922e6d21e8fd8992aa881ba5d`  
		Last Modified: Thu, 02 May 2024 01:51:52 GMT  
		Size: 145.1 MB (145095087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa30e0bc3f6c2ccfdf0951cee89e2b0593d106ded99ebbd8c12cc7663c130ac`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873a66af9faccde7bfd9293d66333f2cdfc34fe0bc05e0232eacb211d48983f`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26209796074bd6bc871da2c60e1872c271baddbddf8d913759ec003da80b4c61`  
		Last Modified: Thu, 02 May 2024 01:51:55 GMT  
		Size: 384.2 MB (384218824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e49bbd140e7db653fb626e909a5ee719a50587557a9c7a9bfdcd8ae54d5f801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf7a4e6d79ae6ac9a83931e855e6a98691cc81b7c92b96c014a50796797fbc`

```dockerfile
```

-	Layers:
	-	`sha256:32dd6421b7e506a5f4213a62dedb3593dccf9d3db2460dba8d93c56bbd198d35`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.1 MB (3127644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61543321fd341dbb90794a30fe6c0c8c8d9be9e3db99c09dac3a6f48ff5dd6b`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise` - linux; arm64 variant v8

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

### `neo4j:5.19.0-enterprise` - unknown; unknown

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

## `neo4j:5.19.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4dcb01cbb1fd8c3d43592557d904068e0f912c102685863bdcc921625aff6e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:52e88b3d625dac9f6c5ae4420534dbb4df6000c0df097232d34e17676e0a62a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59da8fc4fdd58b2d9c2b4ff053a53219b0835d3f0e28390cbc36ac7f56b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb644f90a595a86ac6a3d87c40742d500e6843f922e6d21e8fd8992aa881ba5d`  
		Last Modified: Thu, 02 May 2024 01:51:52 GMT  
		Size: 145.1 MB (145095087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa30e0bc3f6c2ccfdf0951cee89e2b0593d106ded99ebbd8c12cc7663c130ac`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873a66af9faccde7bfd9293d66333f2cdfc34fe0bc05e0232eacb211d48983f`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26209796074bd6bc871da2c60e1872c271baddbddf8d913759ec003da80b4c61`  
		Last Modified: Thu, 02 May 2024 01:51:55 GMT  
		Size: 384.2 MB (384218824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e49bbd140e7db653fb626e909a5ee719a50587557a9c7a9bfdcd8ae54d5f801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf7a4e6d79ae6ac9a83931e855e6a98691cc81b7c92b96c014a50796797fbc`

```dockerfile
```

-	Layers:
	-	`sha256:32dd6421b7e506a5f4213a62dedb3593dccf9d3db2460dba8d93c56bbd198d35`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.1 MB (3127644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61543321fd341dbb90794a30fe6c0c8c8d9be9e3db99c09dac3a6f48ff5dd6b`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise-bullseye` - linux; arm64 variant v8

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

### `neo4j:5.19.0-enterprise-bullseye` - unknown; unknown

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

## `neo4j:5.19.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4b46fa568dd07658aa91edb82a39cd6ab1da29594e85f0e64a7b6b34852cdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:27147d063acb685ad1fa5ff0f3a8830474951d837c10dc25d12c686a96c0d07c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:17aae81547e1f67437f422bbe8b4905143a7ee0130addebe0a5f9af4d4c0fabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545903582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ae3416e60e7423ed433a1975976791ac0afa84938c3c7ec8ebc24cc155212`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779ab28fbb304705ac05e7124f76e128ac2b417e433def98b2e03a28a308cea8`  
		Last Modified: Thu, 02 May 2024 23:53:01 GMT  
		Size: 125.7 MB (125724901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ad1a153a6a805f6b821110ff771e59cabedcce497121a9a83973c0666561d5`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2224f4f7fb46927c2ed3be5d3cdf8eed6d022dfb815480eec737ac4c1f2d`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 381.3 MB (381283629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5cf351076202fa7c397d8c19e02c3365d655080504bdfc54d74bfe53cc2c462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e131ec1c4e1df19bac37b93cf6535326f7c0ad15c7dcb95d3a4861859914ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:e8a7df93cf7344a2ca85dc52ba52955082fd0add9b94f3b7d2502e8703e2f254`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 5.6 MB (5596528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f149ddd3a2723a5e89cc68e33c6012f5a23df12df780b5f0d1109b5d964b1a10`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 20.5 KB (20487 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13ab96e07f5567a7dfe1100c550f5b9b66864ffd205a3aedf9f11e9e59a99283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.2 MB (544165548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f842f62f69ce0ae41172018a2e6b2c8db7374e49fa38f93e780c1d766912084`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c25209986e4a6b63e445440325ed351ffe62ba63f57b21bd1a5613db5f2046`  
		Last Modified: Fri, 03 May 2024 02:17:13 GMT  
		Size: 381.3 MB (381283646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c16bad0ddae11ed55105766602ae734f27c06968bd5a2b9453372fd4b2ebed42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5589831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e757531780f5d911f441c92cad7c2f487c14d6ce80f602efcbbacde450816d4`

```dockerfile
```

-	Layers:
	-	`sha256:e7d8614de5e7ffd06d00b3824b584b3e3a2f007cf7008b5258c939717f9d9e6d`  
		Last Modified: Fri, 03 May 2024 02:17:05 GMT  
		Size: 5.6 MB (5569500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30df46436cf08a463dad8f67c3aaa509f8e9de361944e584be15209455b466cc`  
		Last Modified: Fri, 03 May 2024 02:17:05 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-ubi9`

```console
$ docker pull neo4j@sha256:0370858e78423be0df5631d3e15a9240fdb4f35c42990463f539aa2a481ce46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:2a6ab281aa79fec880ea0e862ee98b67102bd7d212a58192bf6e6fe9b850cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287447087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe745bce68aedcc89238cc1a54d2d36f3b975c1f6819fc9278cda1a3064c2b07`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff05d8cb69b295f1af1e76641afb4691e2b93717cc840209cc62b290660ce9`  
		Last Modified: Thu, 02 May 2024 23:53:09 GMT  
		Size: 125.7 MB (125724994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d428b6aac31517b14c31ad9a634a823c6bba17c66952e5e54e3bf678c5c06c`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad504d95aab247d56384379e3edd2738684943318c763509723ce7e7680c83e0`  
		Last Modified: Thu, 02 May 2024 23:53:08 GMT  
		Size: 122.8 MB (122827043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2edcd2b61e533ecce8fb6ff0414237cbfd2676db105a642b7d7bba5b5c072e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb465354dffe507ece70f10f36380ab315b0e9b14ec9dc67ddc71261e9a78d7`

```dockerfile
```

-	Layers:
	-	`sha256:ddf95c3c44a1aecdf0844d99c9fd06c3c5ff1f32f054478d0bcc1c7d6b54c8d5`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8869c27f54df932f01dbb439c3cf9b6c1b441875aea1af33dcfc6937531bd`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7305b5dd392fb2af49bf1c34bdf80b2e4eea03ac4a3536eb57cdffa736d43b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285708915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c352a0746c8292b35ea8fb2dccc007ee013a355d9efb72e5b80dadffb13f115b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f5f71f9a33e678f6bb048d024e0f49df09d3969eab9252357da8132a3ed`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 122.8 MB (122827013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e7dfe92615851220bfc32bc73235b75a14ff18fa815979efc8d28f9c5626ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f5f903abc3abea14bc8d514c7cb77828d1f4d88873b8286405b57ee8b9908`

```dockerfile
```

-	Layers:
	-	`sha256:594b8f5fd581daf798dcb8933a5ed92b8a225c68583feb07384e1dafc83a6c3f`  
		Last Modified: Fri, 03 May 2024 01:53:06 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070b1734dd9ff6e261e929866fbea0f41e7750384b3f087d69b593e0f76301e`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:0370858e78423be0df5631d3e15a9240fdb4f35c42990463f539aa2a481ce46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:2a6ab281aa79fec880ea0e862ee98b67102bd7d212a58192bf6e6fe9b850cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287447087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe745bce68aedcc89238cc1a54d2d36f3b975c1f6819fc9278cda1a3064c2b07`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff05d8cb69b295f1af1e76641afb4691e2b93717cc840209cc62b290660ce9`  
		Last Modified: Thu, 02 May 2024 23:53:09 GMT  
		Size: 125.7 MB (125724994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d428b6aac31517b14c31ad9a634a823c6bba17c66952e5e54e3bf678c5c06c`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad504d95aab247d56384379e3edd2738684943318c763509723ce7e7680c83e0`  
		Last Modified: Thu, 02 May 2024 23:53:08 GMT  
		Size: 122.8 MB (122827043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2edcd2b61e533ecce8fb6ff0414237cbfd2676db105a642b7d7bba5b5c072e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb465354dffe507ece70f10f36380ab315b0e9b14ec9dc67ddc71261e9a78d7`

```dockerfile
```

-	Layers:
	-	`sha256:ddf95c3c44a1aecdf0844d99c9fd06c3c5ff1f32f054478d0bcc1c7d6b54c8d5`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8869c27f54df932f01dbb439c3cf9b6c1b441875aea1af33dcfc6937531bd`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7305b5dd392fb2af49bf1c34bdf80b2e4eea03ac4a3536eb57cdffa736d43b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285708915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c352a0746c8292b35ea8fb2dccc007ee013a355d9efb72e5b80dadffb13f115b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f5f71f9a33e678f6bb048d024e0f49df09d3969eab9252357da8132a3ed`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 122.8 MB (122827013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e7dfe92615851220bfc32bc73235b75a14ff18fa815979efc8d28f9c5626ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f5f903abc3abea14bc8d514c7cb77828d1f4d88873b8286405b57ee8b9908`

```dockerfile
```

-	Layers:
	-	`sha256:594b8f5fd581daf798dcb8933a5ed92b8a225c68583feb07384e1dafc83a6c3f`  
		Last Modified: Fri, 03 May 2024 01:53:06 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070b1734dd9ff6e261e929866fbea0f41e7750384b3f087d69b593e0f76301e`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:4dcb01cbb1fd8c3d43592557d904068e0f912c102685863bdcc921625aff6e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:52e88b3d625dac9f6c5ae4420534dbb4df6000c0df097232d34e17676e0a62a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59da8fc4fdd58b2d9c2b4ff053a53219b0835d3f0e28390cbc36ac7f56b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb644f90a595a86ac6a3d87c40742d500e6843f922e6d21e8fd8992aa881ba5d`  
		Last Modified: Thu, 02 May 2024 01:51:52 GMT  
		Size: 145.1 MB (145095087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa30e0bc3f6c2ccfdf0951cee89e2b0593d106ded99ebbd8c12cc7663c130ac`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873a66af9faccde7bfd9293d66333f2cdfc34fe0bc05e0232eacb211d48983f`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26209796074bd6bc871da2c60e1872c271baddbddf8d913759ec003da80b4c61`  
		Last Modified: Thu, 02 May 2024 01:51:55 GMT  
		Size: 384.2 MB (384218824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e49bbd140e7db653fb626e909a5ee719a50587557a9c7a9bfdcd8ae54d5f801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf7a4e6d79ae6ac9a83931e855e6a98691cc81b7c92b96c014a50796797fbc`

```dockerfile
```

-	Layers:
	-	`sha256:32dd6421b7e506a5f4213a62dedb3593dccf9d3db2460dba8d93c56bbd198d35`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.1 MB (3127644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61543321fd341dbb90794a30fe6c0c8c8d9be9e3db99c09dac3a6f48ff5dd6b`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
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

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4dcb01cbb1fd8c3d43592557d904068e0f912c102685863bdcc921625aff6e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:52e88b3d625dac9f6c5ae4420534dbb4df6000c0df097232d34e17676e0a62a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59da8fc4fdd58b2d9c2b4ff053a53219b0835d3f0e28390cbc36ac7f56b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb644f90a595a86ac6a3d87c40742d500e6843f922e6d21e8fd8992aa881ba5d`  
		Last Modified: Thu, 02 May 2024 01:51:52 GMT  
		Size: 145.1 MB (145095087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa30e0bc3f6c2ccfdf0951cee89e2b0593d106ded99ebbd8c12cc7663c130ac`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873a66af9faccde7bfd9293d66333f2cdfc34fe0bc05e0232eacb211d48983f`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26209796074bd6bc871da2c60e1872c271baddbddf8d913759ec003da80b4c61`  
		Last Modified: Thu, 02 May 2024 01:51:55 GMT  
		Size: 384.2 MB (384218824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e49bbd140e7db653fb626e909a5ee719a50587557a9c7a9bfdcd8ae54d5f801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cf7a4e6d79ae6ac9a83931e855e6a98691cc81b7c92b96c014a50796797fbc`

```dockerfile
```

-	Layers:
	-	`sha256:32dd6421b7e506a5f4213a62dedb3593dccf9d3db2460dba8d93c56bbd198d35`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 3.1 MB (3127644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61543321fd341dbb90794a30fe6c0c8c8d9be9e3db99c09dac3a6f48ff5dd6b`  
		Last Modified: Thu, 02 May 2024 01:51:49 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

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

### `neo4j:enterprise-bullseye` - unknown; unknown

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

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4b46fa568dd07658aa91edb82a39cd6ab1da29594e85f0e64a7b6b34852cdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:27147d063acb685ad1fa5ff0f3a8830474951d837c10dc25d12c686a96c0d07c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:17aae81547e1f67437f422bbe8b4905143a7ee0130addebe0a5f9af4d4c0fabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545903582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ae3416e60e7423ed433a1975976791ac0afa84938c3c7ec8ebc24cc155212`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779ab28fbb304705ac05e7124f76e128ac2b417e433def98b2e03a28a308cea8`  
		Last Modified: Thu, 02 May 2024 23:53:01 GMT  
		Size: 125.7 MB (125724901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ad1a153a6a805f6b821110ff771e59cabedcce497121a9a83973c0666561d5`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2224f4f7fb46927c2ed3be5d3cdf8eed6d022dfb815480eec737ac4c1f2d`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 381.3 MB (381283629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5cf351076202fa7c397d8c19e02c3365d655080504bdfc54d74bfe53cc2c462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e131ec1c4e1df19bac37b93cf6535326f7c0ad15c7dcb95d3a4861859914ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:e8a7df93cf7344a2ca85dc52ba52955082fd0add9b94f3b7d2502e8703e2f254`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 5.6 MB (5596528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f149ddd3a2723a5e89cc68e33c6012f5a23df12df780b5f0d1109b5d964b1a10`  
		Last Modified: Thu, 02 May 2024 23:52:59 GMT  
		Size: 20.5 KB (20487 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13ab96e07f5567a7dfe1100c550f5b9b66864ffd205a3aedf9f11e9e59a99283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.2 MB (544165548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f842f62f69ce0ae41172018a2e6b2c8db7374e49fa38f93e780c1d766912084`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c25209986e4a6b63e445440325ed351ffe62ba63f57b21bd1a5613db5f2046`  
		Last Modified: Fri, 03 May 2024 02:17:13 GMT  
		Size: 381.3 MB (381283646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c16bad0ddae11ed55105766602ae734f27c06968bd5a2b9453372fd4b2ebed42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5589831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e757531780f5d911f441c92cad7c2f487c14d6ce80f602efcbbacde450816d4`

```dockerfile
```

-	Layers:
	-	`sha256:e7d8614de5e7ffd06d00b3824b584b3e3a2f007cf7008b5258c939717f9d9e6d`  
		Last Modified: Fri, 03 May 2024 02:17:05 GMT  
		Size: 5.6 MB (5569500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30df46436cf08a463dad8f67c3aaa509f8e9de361944e584be15209455b466cc`  
		Last Modified: Fri, 03 May 2024 02:17:05 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:6087e02d37d56e9810fd625bcf9516226cb42560e94baacc1bf251954b4a184a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:0a45fb8f87475ef9aa0ab21a54c38f2f27e7638853fe07be9965573510695fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8445a8313d7396e3492b8911534f0f49653b62a3e9455989de0fc126142c9d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7494cfc3e8a5e9c0ba072adbd10806c69e0cdc2c654a2a6355433a41330b96a`  
		Last Modified: Thu, 02 May 2024 01:51:36 GMT  
		Size: 145.1 MB (145095077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdf3e6f6f756adc3e30d77949e9e67b3de44e7e6d48e08c935b454e21ad79c`  
		Last Modified: Thu, 02 May 2024 01:51:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88997e723e9ebf2a2c92999b95f58ad337af7243c5466986a31dea880ee18d8a`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eade7dccad61f2662e87448836130d677d5380185c393eccd0958cf5211656`  
		Last Modified: Thu, 02 May 2024 01:51:37 GMT  
		Size: 125.8 MB (125760103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:669d5317af3c38551de51c737d8f400d75b45e772bc494c724cdb246a979e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359989597d4dde75cff65650ecfc5d5fc431e475ae3bb2b1647f616e4a66ab28`

```dockerfile
```

-	Layers:
	-	`sha256:da8acc4a3bcd0dba796897be398f2d3bfe1feb2cf4915c71006acc33c7c43374`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 3.0 MB (2959705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe0d54fa26b750f134385a855cd09746a0e681a37f29b0943f10c381948d04d`  
		Last Modified: Thu, 02 May 2024 01:51:34 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2043bccc52b2f70b450dd0e53c22acbdfbde0d9eabfa100cab3cc0098421371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299715319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235a2e7061cb1935a2e81c0e97933aa45f716b21b7ade12bc07d36faf3684`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
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
	-	`sha256:4b51b29f0a1e57324f9432e143d3ee40b85c2f1bcfa8293b0bef3bddccb1d810`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586f98a0a83084a4b814258bae894e5956c733736f96fd4a9b1c58714b2b69d`  
		Last Modified: Thu, 02 May 2024 12:30:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee98ab2716c654d83ea6b67fe11a09d44e3db1e7f51fa4869596191bab0f2565`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 125.7 MB (125721848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:8478bd3cfbdf69da0b337f2cbabbd4408b6c7e917fe00cf535bc57275d0089d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c4b4505535d954f77fd35ceaab76a3247e9c8c20e6a4f3f3579ce96c865d3`

```dockerfile
```

-	Layers:
	-	`sha256:95dbe2d9fe72ce988f695e4003f047096253ff5191459961d2f9a14b9de59342`  
		Last Modified: Thu, 02 May 2024 12:31:00 GMT  
		Size: 3.0 MB (2959947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d71c174f00a80fc505dd27c82285cc79dce0f31a23a0e4d6371e7bcac7fa26`  
		Last Modified: Thu, 02 May 2024 12:30:58 GMT  
		Size: 24.1 KB (24132 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:0370858e78423be0df5631d3e15a9240fdb4f35c42990463f539aa2a481ce46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:2a6ab281aa79fec880ea0e862ee98b67102bd7d212a58192bf6e6fe9b850cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287447087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe745bce68aedcc89238cc1a54d2d36f3b975c1f6819fc9278cda1a3064c2b07`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff05d8cb69b295f1af1e76641afb4691e2b93717cc840209cc62b290660ce9`  
		Last Modified: Thu, 02 May 2024 23:53:09 GMT  
		Size: 125.7 MB (125724994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d428b6aac31517b14c31ad9a634a823c6bba17c66952e5e54e3bf678c5c06c`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad504d95aab247d56384379e3edd2738684943318c763509723ce7e7680c83e0`  
		Last Modified: Thu, 02 May 2024 23:53:08 GMT  
		Size: 122.8 MB (122827043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2edcd2b61e533ecce8fb6ff0414237cbfd2676db105a642b7d7bba5b5c072e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb465354dffe507ece70f10f36380ab315b0e9b14ec9dc67ddc71261e9a78d7`

```dockerfile
```

-	Layers:
	-	`sha256:ddf95c3c44a1aecdf0844d99c9fd06c3c5ff1f32f054478d0bcc1c7d6b54c8d5`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8869c27f54df932f01dbb439c3cf9b6c1b441875aea1af33dcfc6937531bd`  
		Last Modified: Thu, 02 May 2024 23:53:05 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7305b5dd392fb2af49bf1c34bdf80b2e4eea03ac4a3536eb57cdffa736d43b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285708915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c352a0746c8292b35ea8fb2dccc007ee013a355d9efb72e5b80dadffb13f115b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=949
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9a7f125fc912859525837082ece8dac76804800717eaf1393bd4e71bfd9ce`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 125.7 MB (125740749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714ce1c766cf90bc1a8e62e7a387a88cfbad03240a6617918ab439a07f6fbea`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f5f71f9a33e678f6bb048d024e0f49df09d3969eab9252357da8132a3ed`  
		Last Modified: Fri, 03 May 2024 01:53:08 GMT  
		Size: 122.8 MB (122827013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e7dfe92615851220bfc32bc73235b75a14ff18fa815979efc8d28f9c5626ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478f5f903abc3abea14bc8d514c7cb77828d1f4d88873b8286405b57ee8b9908`

```dockerfile
```

-	Layers:
	-	`sha256:594b8f5fd581daf798dcb8933a5ed92b8a225c68583feb07384e1dafc83a6c3f`  
		Last Modified: Fri, 03 May 2024 01:53:06 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f070b1734dd9ff6e261e929866fbea0f41e7750384b3f087d69b593e0f76301e`  
		Last Modified: Fri, 03 May 2024 01:53:05 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json
