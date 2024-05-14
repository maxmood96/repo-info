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
$ docker pull neo4j@sha256:e5c88c6f013770942d15603a8982a191ce7e6b7dabd8c22f80f952a818ed6e01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:9981de65d5e25e85a66584312944e18e5520836d8bc178f3170de11e6acd18e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297972219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd9db54b6548a473261d893816755b9f6cf777c54455ebbfb86760b8918b614`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 09:36:34 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Wed, 24 Apr 2024 09:36:34 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bee7276b0bee5e9c2e82ef59a582555faa02693b21f71e978f07c163cb2cff`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 145.5 MB (145504843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c1c6cc5d32124cc53970d50af79880b0a05a65adca8582373856c8369bf91`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03809805757465989720c06d421524d83e30ca73ff3b0041bcef8457a740d53`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d461a682cd21c913f4261c8c327b6f4be3083300e2a70d0a8ee2e8b67022079f`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 121.0 MB (121020131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:f94e94868f98a9896e6a22c3e0906341da1a2208f3c1524a984f25d9f7c3e763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f1401e50a3516b17eeea80f7a04ecb6b73fb7ba66b3fd8e2aad9a4fb631549`

```dockerfile
```

-	Layers:
	-	`sha256:b6de061b417cc71c1e5238a0a7aceae784a037216eacc54cc147305d2d4a68ec`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 2.9 MB (2940191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970298630101e4725ef0e9a3f685722f5d098fb7b107d71315d3b5fde6eab305`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 20.5 KB (20471 bytes)  
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
$ docker pull neo4j@sha256:e5c88c6f013770942d15603a8982a191ce7e6b7dabd8c22f80f952a818ed6e01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9981de65d5e25e85a66584312944e18e5520836d8bc178f3170de11e6acd18e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297972219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd9db54b6548a473261d893816755b9f6cf777c54455ebbfb86760b8918b614`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 09:36:34 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Wed, 24 Apr 2024 09:36:34 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bee7276b0bee5e9c2e82ef59a582555faa02693b21f71e978f07c163cb2cff`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 145.5 MB (145504843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c1c6cc5d32124cc53970d50af79880b0a05a65adca8582373856c8369bf91`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03809805757465989720c06d421524d83e30ca73ff3b0041bcef8457a740d53`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d461a682cd21c913f4261c8c327b6f4be3083300e2a70d0a8ee2e8b67022079f`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 121.0 MB (121020131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:f94e94868f98a9896e6a22c3e0906341da1a2208f3c1524a984f25d9f7c3e763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f1401e50a3516b17eeea80f7a04ecb6b73fb7ba66b3fd8e2aad9a4fb631549`

```dockerfile
```

-	Layers:
	-	`sha256:b6de061b417cc71c1e5238a0a7aceae784a037216eacc54cc147305d2d4a68ec`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 2.9 MB (2940191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970298630101e4725ef0e9a3f685722f5d098fb7b107d71315d3b5fde6eab305`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 20.5 KB (20471 bytes)  
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
$ docker pull neo4j@sha256:99d4943379eccc38967f382d3b7ef250ed7f105d254fb5d66d5549f3341bddf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:cd5ecd034afba4e6bde15f8643a98ac4562ae806e0371d83801ad531c88bf1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402700706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60ac6a1eab2cd74e665917279d1371a66f7d81e2f9db6d2005986b1c5c4ddd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 09:36:34 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Wed, 24 Apr 2024 09:36:34 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0852163fab5f17c61ad73aabb59ae54aeea698ca0612d3eb05593562dc2c79`  
		Last Modified: Tue, 14 May 2024 02:56:41 GMT  
		Size: 145.5 MB (145504828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f07466fb9e9f4b6e0e0a1d6684aae49f02f7c9fe0a231e4c761e0f7c5cad0`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0346d8aa5d8b6d4d9f444ac03cd3cf0a56af1c4e9b16ff2823e24ac0cad6f31`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ac380fd544233f228c3ed8768ba2913a4c0380e2d9033e95146b8960d536b0`  
		Last Modified: Tue, 14 May 2024 02:56:41 GMT  
		Size: 225.7 MB (225748636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:bef3a6d335cc6679cde928f3ecef38e615bb4e62f40c6e1f9a298e77599c4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbda3dd560ad2ead35d6173799e231ade71f51cde55c136cd75c2d37b5e0731`

```dockerfile
```

-	Layers:
	-	`sha256:f036e5b6474c25696fe203ab4d9af1076f00cad6f9e6e48d43fe2cdf71ce15f0`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.1 MB (3069501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1bd2e0fd5ae2d376d968c36e0177bd106bb2dfd0377774df98963044cbfbd2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
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
$ docker pull neo4j@sha256:e5c88c6f013770942d15603a8982a191ce7e6b7dabd8c22f80f952a818ed6e01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.33` - linux; amd64

```console
$ docker pull neo4j@sha256:9981de65d5e25e85a66584312944e18e5520836d8bc178f3170de11e6acd18e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297972219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd9db54b6548a473261d893816755b9f6cf777c54455ebbfb86760b8918b614`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 09:36:34 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Wed, 24 Apr 2024 09:36:34 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bee7276b0bee5e9c2e82ef59a582555faa02693b21f71e978f07c163cb2cff`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 145.5 MB (145504843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c1c6cc5d32124cc53970d50af79880b0a05a65adca8582373856c8369bf91`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03809805757465989720c06d421524d83e30ca73ff3b0041bcef8457a740d53`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d461a682cd21c913f4261c8c327b6f4be3083300e2a70d0a8ee2e8b67022079f`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 121.0 MB (121020131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33` - unknown; unknown

```console
$ docker pull neo4j@sha256:f94e94868f98a9896e6a22c3e0906341da1a2208f3c1524a984f25d9f7c3e763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f1401e50a3516b17eeea80f7a04ecb6b73fb7ba66b3fd8e2aad9a4fb631549`

```dockerfile
```

-	Layers:
	-	`sha256:b6de061b417cc71c1e5238a0a7aceae784a037216eacc54cc147305d2d4a68ec`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 2.9 MB (2940191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970298630101e4725ef0e9a3f685722f5d098fb7b107d71315d3b5fde6eab305`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 20.5 KB (20471 bytes)  
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
$ docker pull neo4j@sha256:e5c88c6f013770942d15603a8982a191ce7e6b7dabd8c22f80f952a818ed6e01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.33-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9981de65d5e25e85a66584312944e18e5520836d8bc178f3170de11e6acd18e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297972219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd9db54b6548a473261d893816755b9f6cf777c54455ebbfb86760b8918b614`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 09:36:34 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Wed, 24 Apr 2024 09:36:34 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bee7276b0bee5e9c2e82ef59a582555faa02693b21f71e978f07c163cb2cff`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 145.5 MB (145504843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c1c6cc5d32124cc53970d50af79880b0a05a65adca8582373856c8369bf91`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03809805757465989720c06d421524d83e30ca73ff3b0041bcef8457a740d53`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d461a682cd21c913f4261c8c327b6f4be3083300e2a70d0a8ee2e8b67022079f`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 121.0 MB (121020131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:f94e94868f98a9896e6a22c3e0906341da1a2208f3c1524a984f25d9f7c3e763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f1401e50a3516b17eeea80f7a04ecb6b73fb7ba66b3fd8e2aad9a4fb631549`

```dockerfile
```

-	Layers:
	-	`sha256:b6de061b417cc71c1e5238a0a7aceae784a037216eacc54cc147305d2d4a68ec`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 2.9 MB (2940191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970298630101e4725ef0e9a3f685722f5d098fb7b107d71315d3b5fde6eab305`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 20.5 KB (20471 bytes)  
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
$ docker pull neo4j@sha256:99d4943379eccc38967f382d3b7ef250ed7f105d254fb5d66d5549f3341bddf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.33-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:cd5ecd034afba4e6bde15f8643a98ac4562ae806e0371d83801ad531c88bf1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402700706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60ac6a1eab2cd74e665917279d1371a66f7d81e2f9db6d2005986b1c5c4ddd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Apr 2024 09:36:34 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Wed, 24 Apr 2024 09:36:34 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0852163fab5f17c61ad73aabb59ae54aeea698ca0612d3eb05593562dc2c79`  
		Last Modified: Tue, 14 May 2024 02:56:41 GMT  
		Size: 145.5 MB (145504828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f07466fb9e9f4b6e0e0a1d6684aae49f02f7c9fe0a231e4c761e0f7c5cad0`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0346d8aa5d8b6d4d9f444ac03cd3cf0a56af1c4e9b16ff2823e24ac0cad6f31`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ac380fd544233f228c3ed8768ba2913a4c0380e2d9033e95146b8960d536b0`  
		Last Modified: Tue, 14 May 2024 02:56:41 GMT  
		Size: 225.7 MB (225748636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.33-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:bef3a6d335cc6679cde928f3ecef38e615bb4e62f40c6e1f9a298e77599c4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbda3dd560ad2ead35d6173799e231ade71f51cde55c136cd75c2d37b5e0731`

```dockerfile
```

-	Layers:
	-	`sha256:f036e5b6474c25696fe203ab4d9af1076f00cad6f9e6e48d43fe2cdf71ce15f0`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.1 MB (3069501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1bd2e0fd5ae2d376d968c36e0177bd106bb2dfd0377774df98963044cbfbd2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:e23e34f9896590da03904aab954edb6d821c95b8511c06952a2d8f698de42c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:cff54c32b9b96e08d1d0b5dbb5f6490ac6e0e88902df64d9f30371108e199df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98145555cd08f53fe064fc227ac2ab3c96dc928d6657cbb27bc7d47070b5ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214bad9fa2f0fbd9a87ce5a23845cd04f89f4e86961aac8acd64a58dbe30b07`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 152.3 MB (152305645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b2eca8bc53ccdaab4b9ab7630b460cc954cf7ffb71032e216713d480f03cf`  
		Last Modified: Fri, 10 May 2024 18:52:03 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f004ce17c2711163aa4dccc17ff88d46e8cdc9fbc023d1cadcd53eee9acd6fb`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 122.8 MB (122827183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:067a39758bc6681c95806007ba09712782f16589dc8d464b60a69cc970fca60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a37c28eb797dcbf15a37e86b6e807c740d382b377b077c9c871bb2b07aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:78cd8ee210804509043c19674c3c534b158201d3475416a621d6aa660fd88e27`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 10.3 MB (10306841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056a2250cdef3123d1991d52063d48244dc9ffbdce9464c7c1f12515ae4232ab`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:ca2fbd072605f1e11c4a2bf7255993d7fca17375a849a11273083ba2d03a3c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c581706f1e6805e4ae0b9935e0c043f589e3760d99f631dc676094d5f2234021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287452952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118790adc66481a526e9b265d1a2e8c91cc151754e69952cef6f92852166734`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53976c770d79e6e3138db213e11cfe0086c4477ef0b1d7634595540cfc6e6b68`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 125.7 MB (125729612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573c66f11ba008460aeb70413941404cd1c3d56c60aff4fdfa89b3289cdc029`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca36784ab94d19d0fbae65461337e24b35ff2bb1f4f35c9c7d71bba918dcec1`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 122.8 MB (122827037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:79a931143aa0f9c6d26372bf483515e4b5069748f5f73a433356bd52ba72964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d0f6120b4e7153fbdbc0f3f875e3c16c6203a6ffb9e4add1e1964f0ccdf20`

```dockerfile
```

-	Layers:
	-	`sha256:0e2db2e554b686f53b839594c05a93a8320d063208d56e01c6414372e6fb48e3`  
		Last Modified: Tue, 07 May 2024 21:52:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea6a2f7274e247e814c49afe2132b83c36742235783e71391ed1766cb968209`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02af71e50a215ff6633db917db2c0b4bae54000d5770988f08cc68e2b078d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43023c34a2aadd531e4c000d6addf90fd608a11d26b8174ffa82ed471d70472`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8723f7f09ed20f0ed179310b9ae5849e8e613e8784a81a22b9456410507166`  
		Last Modified: Wed, 08 May 2024 02:03:01 GMT  
		Size: 122.8 MB (122827004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:72eb84817ce787bc4485c8e188f950c380ee56ac9dd620ee2f6513f4175ced87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ee49faec0f84760062cf258edcae05e956fb58861e35695c83b82a0cb1270d`

```dockerfile
```

-	Layers:
	-	`sha256:95c2a060b0815de5e11bb9fd7bd737a4ad7667598b7e22d92e35c4f8ac05e996`  
		Last Modified: Wed, 08 May 2024 02:02:59 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c9fe20d7cfa9fbd00b6439168f2651bfda07ffbf00cbadec6d33b9f2f7788`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:8552defe4b2f5325389337291f1afc7e47caa19e371d44f76d934da92e87ca23
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
$ docker pull neo4j@sha256:8552defe4b2f5325389337291f1afc7e47caa19e371d44f76d934da92e87ca23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

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

### `neo4j:5-enterprise-bullseye` - unknown; unknown

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
$ docker pull neo4j@sha256:cd4375dca32fdd8484fcfa93b7074b3aa42e490d413e21ed5296b7eee1776895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:696b1068794b2f69e3ed264a9ac5dc631f441358891d926a2519228de6d4cfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.9 MB (572889686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae32533ac43845337108943452af4ea00c706fb0f9212c36bd4d219ed1b511`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98735785b25cc20b3c023ddb1bda8b3d2989ef8ccca7f146055e478cc25ca41`  
		Last Modified: Fri, 10 May 2024 18:52:11 GMT  
		Size: 152.3 MB (152305137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0dcd874afd2fb773e8f9a7b71be53436223e3b6319bd4288218758b2ed802`  
		Last Modified: Fri, 10 May 2024 18:52:09 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12bcb4da80bea0eaec8659de89316cdb885c7b1d0298436b229e6318cfc78f1`  
		Last Modified: Fri, 10 May 2024 18:52:16 GMT  
		Size: 381.3 MB (381284032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:678d61b655e61bd335dbbd557f1fbed392850856d7995401ead0c80a9edcbf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e976e5c2c0c3e556a2f1cc1bc212393dcbfd7caca671f1d2c010c293d7567a26`

```dockerfile
```

-	Layers:
	-	`sha256:01be8535193e29b9f22377f2281b32edbb09f7e13e72a61120b742508899232c`  
		Last Modified: Fri, 10 May 2024 18:52:10 GMT  
		Size: 10.5 MB (10475974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53004001571e0cb476b680e6f7d8b602305b23f76a9ca9e505237802fd32500f`  
		Last Modified: Fri, 10 May 2024 18:52:10 GMT  
		Size: 20.5 KB (20462 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0787c0261a75dfc6cf0dcca7c91d065cdbddf9dbb5a0881529fdc0ba1df37301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569929600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587c79223d4802351010c078db542011a0f857600271cfd3c3faef74aea491fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb64181e0a6ee5bc4621f7fdcbc258f924a917ed5d78ea57a8efec65e186e129`  
		Last Modified: Fri, 10 May 2024 19:18:59 GMT  
		Size: 381.3 MB (381284078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:74eed8a6dc09311522cc523213450983f04e5ada8ebd962b1e7cd36e3914d342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10493817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8872159f066f8956a53d2b389ab74a8947ceeb6946c1b70bf55f1288b7982b79`

```dockerfile
```

-	Layers:
	-	`sha256:a072da0a949c8ba0ad7444b31d957bfae35268f566e7570c7a73cbdb916f3639`  
		Last Modified: Fri, 10 May 2024 19:18:51 GMT  
		Size: 10.5 MB (10473512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76263e58119d5ff9c20eabc9518ba1b15296d52f736f4fc3511ea26862775d9f`  
		Last Modified: Fri, 10 May 2024 19:18:51 GMT  
		Size: 20.3 KB (20305 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9bbcdea01c7b63562da85fb584f62445cb005811a4f773c75ad766aefac94cd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f434c90126e5d2d9ad427e92d7def7d66fa3210c0634f6c6d870ecae702d894a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545909296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb21f9996d62f68c301cf67f2c65d2846a02f034eefe98d9bfee433b227470ea`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3e9d41866091c413f654fc0a05860615b6cddb3817a9ddf4dade67c9e2db7d`  
		Last Modified: Tue, 07 May 2024 21:52:00 GMT  
		Size: 125.7 MB (125729524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304dd60691526542f62607860ee0db40205ea0007d57d0f1457269d1685e76d2`  
		Last Modified: Tue, 07 May 2024 21:51:58 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc51647b3ed161fa625b6c5cda4256f557d40d0ad88ff354056c12f3e15c53bc`  
		Last Modified: Tue, 07 May 2024 21:52:06 GMT  
		Size: 381.3 MB (381283472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4f019b5bb9842c7280e908682599805518af587136b5d7904cc8048d5cc7e529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa465633e4ea0e48642d98ff034836d18e598504c8b70de20b76e41263babb4`

```dockerfile
```

-	Layers:
	-	`sha256:34f7842f0f7dbb9c6ca9de88189cb5b046da2a2f2a61c873fc7bc1f9edb392db`  
		Last Modified: Tue, 07 May 2024 21:51:59 GMT  
		Size: 5.6 MB (5596528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d154c8e4bc881ead54c113d154c30988ce755864b9e90768c0ed77da9f22887`  
		Last Modified: Tue, 07 May 2024 21:51:58 GMT  
		Size: 20.5 KB (20487 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:30f88d0bde554988f0c6c217b8d3c75be4ccc9f2f55bbd7d6a0156809de18940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544129909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60da0bc7666725dee1fd0e6af7117094ef3947ce4c75525c161d5e7a71504867`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a11ba6639e442879d41beacbb496c2919dc04ff18ca854dcd17834055438808`  
		Last Modified: Wed, 08 May 2024 02:38:50 GMT  
		Size: 381.3 MB (381283655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b95009a30fb15d5015406216050c3ad162eb301c295e17b822331a3a46080b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5589831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29238932960c90597d898ea9120e5476fbcea84460982649a7c34c819ccce25`

```dockerfile
```

-	Layers:
	-	`sha256:ebfbb9a45c8f3110a5c6012ba4f90839eaf09c66bcb997471286f50aa7d9f89d`  
		Last Modified: Wed, 08 May 2024 02:38:43 GMT  
		Size: 5.6 MB (5569500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f647e6b7352660a6fa6c0413da7ef6f10128dbdc5091b48028f3e07a77bee77`  
		Last Modified: Wed, 08 May 2024 02:38:42 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:e23e34f9896590da03904aab954edb6d821c95b8511c06952a2d8f698de42c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:cff54c32b9b96e08d1d0b5dbb5f6490ac6e0e88902df64d9f30371108e199df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98145555cd08f53fe064fc227ac2ab3c96dc928d6657cbb27bc7d47070b5ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214bad9fa2f0fbd9a87ce5a23845cd04f89f4e86961aac8acd64a58dbe30b07`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 152.3 MB (152305645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b2eca8bc53ccdaab4b9ab7630b460cc954cf7ffb71032e216713d480f03cf`  
		Last Modified: Fri, 10 May 2024 18:52:03 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f004ce17c2711163aa4dccc17ff88d46e8cdc9fbc023d1cadcd53eee9acd6fb`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 122.8 MB (122827183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:067a39758bc6681c95806007ba09712782f16589dc8d464b60a69cc970fca60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a37c28eb797dcbf15a37e86b6e807c740d382b377b077c9c871bb2b07aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:78cd8ee210804509043c19674c3c534b158201d3475416a621d6aa660fd88e27`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 10.3 MB (10306841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056a2250cdef3123d1991d52063d48244dc9ffbdce9464c7c1f12515ae4232ab`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:ca2fbd072605f1e11c4a2bf7255993d7fca17375a849a11273083ba2d03a3c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c581706f1e6805e4ae0b9935e0c043f589e3760d99f631dc676094d5f2234021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287452952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118790adc66481a526e9b265d1a2e8c91cc151754e69952cef6f92852166734`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53976c770d79e6e3138db213e11cfe0086c4477ef0b1d7634595540cfc6e6b68`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 125.7 MB (125729612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573c66f11ba008460aeb70413941404cd1c3d56c60aff4fdfa89b3289cdc029`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca36784ab94d19d0fbae65461337e24b35ff2bb1f4f35c9c7d71bba918dcec1`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 122.8 MB (122827037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:79a931143aa0f9c6d26372bf483515e4b5069748f5f73a433356bd52ba72964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d0f6120b4e7153fbdbc0f3f875e3c16c6203a6ffb9e4add1e1964f0ccdf20`

```dockerfile
```

-	Layers:
	-	`sha256:0e2db2e554b686f53b839594c05a93a8320d063208d56e01c6414372e6fb48e3`  
		Last Modified: Tue, 07 May 2024 21:52:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea6a2f7274e247e814c49afe2132b83c36742235783e71391ed1766cb968209`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02af71e50a215ff6633db917db2c0b4bae54000d5770988f08cc68e2b078d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43023c34a2aadd531e4c000d6addf90fd608a11d26b8174ffa82ed471d70472`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8723f7f09ed20f0ed179310b9ae5849e8e613e8784a81a22b9456410507166`  
		Last Modified: Wed, 08 May 2024 02:03:01 GMT  
		Size: 122.8 MB (122827004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:72eb84817ce787bc4485c8e188f950c380ee56ac9dd620ee2f6513f4175ced87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ee49faec0f84760062cf258edcae05e956fb58861e35695c83b82a0cb1270d`

```dockerfile
```

-	Layers:
	-	`sha256:95c2a060b0815de5e11bb9fd7bd737a4ad7667598b7e22d92e35c4f8ac05e996`  
		Last Modified: Wed, 08 May 2024 02:02:59 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c9fe20d7cfa9fbd00b6439168f2651bfda07ffbf00cbadec6d33b9f2f7788`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19`

```console
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:e23e34f9896590da03904aab954edb6d821c95b8511c06952a2d8f698de42c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:cff54c32b9b96e08d1d0b5dbb5f6490ac6e0e88902df64d9f30371108e199df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98145555cd08f53fe064fc227ac2ab3c96dc928d6657cbb27bc7d47070b5ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214bad9fa2f0fbd9a87ce5a23845cd04f89f4e86961aac8acd64a58dbe30b07`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 152.3 MB (152305645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b2eca8bc53ccdaab4b9ab7630b460cc954cf7ffb71032e216713d480f03cf`  
		Last Modified: Fri, 10 May 2024 18:52:03 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f004ce17c2711163aa4dccc17ff88d46e8cdc9fbc023d1cadcd53eee9acd6fb`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 122.8 MB (122827183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:067a39758bc6681c95806007ba09712782f16589dc8d464b60a69cc970fca60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a37c28eb797dcbf15a37e86b6e807c740d382b377b077c9c871bb2b07aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:78cd8ee210804509043c19674c3c534b158201d3475416a621d6aa660fd88e27`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 10.3 MB (10306841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056a2250cdef3123d1991d52063d48244dc9ffbdce9464c7c1f12515ae4232ab`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community-ubi9`

```console
$ docker pull neo4j@sha256:ca2fbd072605f1e11c4a2bf7255993d7fca17375a849a11273083ba2d03a3c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c581706f1e6805e4ae0b9935e0c043f589e3760d99f631dc676094d5f2234021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287452952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118790adc66481a526e9b265d1a2e8c91cc151754e69952cef6f92852166734`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53976c770d79e6e3138db213e11cfe0086c4477ef0b1d7634595540cfc6e6b68`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 125.7 MB (125729612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573c66f11ba008460aeb70413941404cd1c3d56c60aff4fdfa89b3289cdc029`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca36784ab94d19d0fbae65461337e24b35ff2bb1f4f35c9c7d71bba918dcec1`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 122.8 MB (122827037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:79a931143aa0f9c6d26372bf483515e4b5069748f5f73a433356bd52ba72964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d0f6120b4e7153fbdbc0f3f875e3c16c6203a6ffb9e4add1e1964f0ccdf20`

```dockerfile
```

-	Layers:
	-	`sha256:0e2db2e554b686f53b839594c05a93a8320d063208d56e01c6414372e6fb48e3`  
		Last Modified: Tue, 07 May 2024 21:52:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea6a2f7274e247e814c49afe2132b83c36742235783e71391ed1766cb968209`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02af71e50a215ff6633db917db2c0b4bae54000d5770988f08cc68e2b078d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43023c34a2aadd531e4c000d6addf90fd608a11d26b8174ffa82ed471d70472`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8723f7f09ed20f0ed179310b9ae5849e8e613e8784a81a22b9456410507166`  
		Last Modified: Wed, 08 May 2024 02:03:01 GMT  
		Size: 122.8 MB (122827004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:72eb84817ce787bc4485c8e188f950c380ee56ac9dd620ee2f6513f4175ced87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ee49faec0f84760062cf258edcae05e956fb58861e35695c83b82a0cb1270d`

```dockerfile
```

-	Layers:
	-	`sha256:95c2a060b0815de5e11bb9fd7bd737a4ad7667598b7e22d92e35c4f8ac05e996`  
		Last Modified: Wed, 08 May 2024 02:02:59 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c9fe20d7cfa9fbd00b6439168f2651bfda07ffbf00cbadec6d33b9f2f7788`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-enterprise`

```console
$ docker pull neo4j@sha256:8552defe4b2f5325389337291f1afc7e47caa19e371d44f76d934da92e87ca23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise` - linux; amd64

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

### `neo4j:5.19-enterprise` - unknown; unknown

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
$ docker pull neo4j@sha256:8552defe4b2f5325389337291f1afc7e47caa19e371d44f76d934da92e87ca23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-bullseye` - linux; amd64

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

### `neo4j:5.19-enterprise-bullseye` - unknown; unknown

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
$ docker pull neo4j@sha256:cd4375dca32fdd8484fcfa93b7074b3aa42e490d413e21ed5296b7eee1776895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:696b1068794b2f69e3ed264a9ac5dc631f441358891d926a2519228de6d4cfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.9 MB (572889686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae32533ac43845337108943452af4ea00c706fb0f9212c36bd4d219ed1b511`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98735785b25cc20b3c023ddb1bda8b3d2989ef8ccca7f146055e478cc25ca41`  
		Last Modified: Fri, 10 May 2024 18:52:11 GMT  
		Size: 152.3 MB (152305137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0dcd874afd2fb773e8f9a7b71be53436223e3b6319bd4288218758b2ed802`  
		Last Modified: Fri, 10 May 2024 18:52:09 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12bcb4da80bea0eaec8659de89316cdb885c7b1d0298436b229e6318cfc78f1`  
		Last Modified: Fri, 10 May 2024 18:52:16 GMT  
		Size: 381.3 MB (381284032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:678d61b655e61bd335dbbd557f1fbed392850856d7995401ead0c80a9edcbf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e976e5c2c0c3e556a2f1cc1bc212393dcbfd7caca671f1d2c010c293d7567a26`

```dockerfile
```

-	Layers:
	-	`sha256:01be8535193e29b9f22377f2281b32edbb09f7e13e72a61120b742508899232c`  
		Last Modified: Fri, 10 May 2024 18:52:10 GMT  
		Size: 10.5 MB (10475974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53004001571e0cb476b680e6f7d8b602305b23f76a9ca9e505237802fd32500f`  
		Last Modified: Fri, 10 May 2024 18:52:10 GMT  
		Size: 20.5 KB (20462 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0787c0261a75dfc6cf0dcca7c91d065cdbddf9dbb5a0881529fdc0ba1df37301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569929600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587c79223d4802351010c078db542011a0f857600271cfd3c3faef74aea491fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb64181e0a6ee5bc4621f7fdcbc258f924a917ed5d78ea57a8efec65e186e129`  
		Last Modified: Fri, 10 May 2024 19:18:59 GMT  
		Size: 381.3 MB (381284078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:74eed8a6dc09311522cc523213450983f04e5ada8ebd962b1e7cd36e3914d342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10493817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8872159f066f8956a53d2b389ab74a8947ceeb6946c1b70bf55f1288b7982b79`

```dockerfile
```

-	Layers:
	-	`sha256:a072da0a949c8ba0ad7444b31d957bfae35268f566e7570c7a73cbdb916f3639`  
		Last Modified: Fri, 10 May 2024 19:18:51 GMT  
		Size: 10.5 MB (10473512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76263e58119d5ff9c20eabc9518ba1b15296d52f736f4fc3511ea26862775d9f`  
		Last Modified: Fri, 10 May 2024 19:18:51 GMT  
		Size: 20.3 KB (20305 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9bbcdea01c7b63562da85fb584f62445cb005811a4f773c75ad766aefac94cd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f434c90126e5d2d9ad427e92d7def7d66fa3210c0634f6c6d870ecae702d894a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545909296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb21f9996d62f68c301cf67f2c65d2846a02f034eefe98d9bfee433b227470ea`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3e9d41866091c413f654fc0a05860615b6cddb3817a9ddf4dade67c9e2db7d`  
		Last Modified: Tue, 07 May 2024 21:52:00 GMT  
		Size: 125.7 MB (125729524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304dd60691526542f62607860ee0db40205ea0007d57d0f1457269d1685e76d2`  
		Last Modified: Tue, 07 May 2024 21:51:58 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc51647b3ed161fa625b6c5cda4256f557d40d0ad88ff354056c12f3e15c53bc`  
		Last Modified: Tue, 07 May 2024 21:52:06 GMT  
		Size: 381.3 MB (381283472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4f019b5bb9842c7280e908682599805518af587136b5d7904cc8048d5cc7e529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa465633e4ea0e48642d98ff034836d18e598504c8b70de20b76e41263babb4`

```dockerfile
```

-	Layers:
	-	`sha256:34f7842f0f7dbb9c6ca9de88189cb5b046da2a2f2a61c873fc7bc1f9edb392db`  
		Last Modified: Tue, 07 May 2024 21:51:59 GMT  
		Size: 5.6 MB (5596528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d154c8e4bc881ead54c113d154c30988ce755864b9e90768c0ed77da9f22887`  
		Last Modified: Tue, 07 May 2024 21:51:58 GMT  
		Size: 20.5 KB (20487 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:30f88d0bde554988f0c6c217b8d3c75be4ccc9f2f55bbd7d6a0156809de18940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544129909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60da0bc7666725dee1fd0e6af7117094ef3947ce4c75525c161d5e7a71504867`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a11ba6639e442879d41beacbb496c2919dc04ff18ca854dcd17834055438808`  
		Last Modified: Wed, 08 May 2024 02:38:50 GMT  
		Size: 381.3 MB (381283655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b95009a30fb15d5015406216050c3ad162eb301c295e17b822331a3a46080b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5589831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29238932960c90597d898ea9120e5476fbcea84460982649a7c34c819ccce25`

```dockerfile
```

-	Layers:
	-	`sha256:ebfbb9a45c8f3110a5c6012ba4f90839eaf09c66bcb997471286f50aa7d9f89d`  
		Last Modified: Wed, 08 May 2024 02:38:43 GMT  
		Size: 5.6 MB (5569500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f647e6b7352660a6fa6c0413da7ef6f10128dbdc5091b48028f3e07a77bee77`  
		Last Modified: Wed, 08 May 2024 02:38:42 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-ubi8`

```console
$ docker pull neo4j@sha256:e23e34f9896590da03904aab954edb6d821c95b8511c06952a2d8f698de42c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:cff54c32b9b96e08d1d0b5dbb5f6490ac6e0e88902df64d9f30371108e199df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98145555cd08f53fe064fc227ac2ab3c96dc928d6657cbb27bc7d47070b5ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214bad9fa2f0fbd9a87ce5a23845cd04f89f4e86961aac8acd64a58dbe30b07`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 152.3 MB (152305645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b2eca8bc53ccdaab4b9ab7630b460cc954cf7ffb71032e216713d480f03cf`  
		Last Modified: Fri, 10 May 2024 18:52:03 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f004ce17c2711163aa4dccc17ff88d46e8cdc9fbc023d1cadcd53eee9acd6fb`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 122.8 MB (122827183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:067a39758bc6681c95806007ba09712782f16589dc8d464b60a69cc970fca60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a37c28eb797dcbf15a37e86b6e807c740d382b377b077c9c871bb2b07aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:78cd8ee210804509043c19674c3c534b158201d3475416a621d6aa660fd88e27`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 10.3 MB (10306841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056a2250cdef3123d1991d52063d48244dc9ffbdce9464c7c1f12515ae4232ab`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-ubi9`

```console
$ docker pull neo4j@sha256:ca2fbd072605f1e11c4a2bf7255993d7fca17375a849a11273083ba2d03a3c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c581706f1e6805e4ae0b9935e0c043f589e3760d99f631dc676094d5f2234021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287452952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118790adc66481a526e9b265d1a2e8c91cc151754e69952cef6f92852166734`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53976c770d79e6e3138db213e11cfe0086c4477ef0b1d7634595540cfc6e6b68`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 125.7 MB (125729612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573c66f11ba008460aeb70413941404cd1c3d56c60aff4fdfa89b3289cdc029`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca36784ab94d19d0fbae65461337e24b35ff2bb1f4f35c9c7d71bba918dcec1`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 122.8 MB (122827037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:79a931143aa0f9c6d26372bf483515e4b5069748f5f73a433356bd52ba72964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d0f6120b4e7153fbdbc0f3f875e3c16c6203a6ffb9e4add1e1964f0ccdf20`

```dockerfile
```

-	Layers:
	-	`sha256:0e2db2e554b686f53b839594c05a93a8320d063208d56e01c6414372e6fb48e3`  
		Last Modified: Tue, 07 May 2024 21:52:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea6a2f7274e247e814c49afe2132b83c36742235783e71391ed1766cb968209`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02af71e50a215ff6633db917db2c0b4bae54000d5770988f08cc68e2b078d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43023c34a2aadd531e4c000d6addf90fd608a11d26b8174ffa82ed471d70472`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8723f7f09ed20f0ed179310b9ae5849e8e613e8784a81a22b9456410507166`  
		Last Modified: Wed, 08 May 2024 02:03:01 GMT  
		Size: 122.8 MB (122827004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:72eb84817ce787bc4485c8e188f950c380ee56ac9dd620ee2f6513f4175ced87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ee49faec0f84760062cf258edcae05e956fb58861e35695c83b82a0cb1270d`

```dockerfile
```

-	Layers:
	-	`sha256:95c2a060b0815de5e11bb9fd7bd737a4ad7667598b7e22d92e35c4f8ac05e996`  
		Last Modified: Wed, 08 May 2024 02:02:59 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c9fe20d7cfa9fbd00b6439168f2651bfda07ffbf00cbadec6d33b9f2f7788`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0`

```console
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:e23e34f9896590da03904aab954edb6d821c95b8511c06952a2d8f698de42c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:cff54c32b9b96e08d1d0b5dbb5f6490ac6e0e88902df64d9f30371108e199df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98145555cd08f53fe064fc227ac2ab3c96dc928d6657cbb27bc7d47070b5ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214bad9fa2f0fbd9a87ce5a23845cd04f89f4e86961aac8acd64a58dbe30b07`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 152.3 MB (152305645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b2eca8bc53ccdaab4b9ab7630b460cc954cf7ffb71032e216713d480f03cf`  
		Last Modified: Fri, 10 May 2024 18:52:03 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f004ce17c2711163aa4dccc17ff88d46e8cdc9fbc023d1cadcd53eee9acd6fb`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 122.8 MB (122827183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:067a39758bc6681c95806007ba09712782f16589dc8d464b60a69cc970fca60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a37c28eb797dcbf15a37e86b6e807c740d382b377b077c9c871bb2b07aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:78cd8ee210804509043c19674c3c534b158201d3475416a621d6aa660fd88e27`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 10.3 MB (10306841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056a2250cdef3123d1991d52063d48244dc9ffbdce9464c7c1f12515ae4232ab`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community-ubi9`

```console
$ docker pull neo4j@sha256:ca2fbd072605f1e11c4a2bf7255993d7fca17375a849a11273083ba2d03a3c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c581706f1e6805e4ae0b9935e0c043f589e3760d99f631dc676094d5f2234021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287452952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118790adc66481a526e9b265d1a2e8c91cc151754e69952cef6f92852166734`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53976c770d79e6e3138db213e11cfe0086c4477ef0b1d7634595540cfc6e6b68`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 125.7 MB (125729612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573c66f11ba008460aeb70413941404cd1c3d56c60aff4fdfa89b3289cdc029`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca36784ab94d19d0fbae65461337e24b35ff2bb1f4f35c9c7d71bba918dcec1`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 122.8 MB (122827037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:79a931143aa0f9c6d26372bf483515e4b5069748f5f73a433356bd52ba72964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d0f6120b4e7153fbdbc0f3f875e3c16c6203a6ffb9e4add1e1964f0ccdf20`

```dockerfile
```

-	Layers:
	-	`sha256:0e2db2e554b686f53b839594c05a93a8320d063208d56e01c6414372e6fb48e3`  
		Last Modified: Tue, 07 May 2024 21:52:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea6a2f7274e247e814c49afe2132b83c36742235783e71391ed1766cb968209`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02af71e50a215ff6633db917db2c0b4bae54000d5770988f08cc68e2b078d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43023c34a2aadd531e4c000d6addf90fd608a11d26b8174ffa82ed471d70472`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8723f7f09ed20f0ed179310b9ae5849e8e613e8784a81a22b9456410507166`  
		Last Modified: Wed, 08 May 2024 02:03:01 GMT  
		Size: 122.8 MB (122827004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:72eb84817ce787bc4485c8e188f950c380ee56ac9dd620ee2f6513f4175ced87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ee49faec0f84760062cf258edcae05e956fb58861e35695c83b82a0cb1270d`

```dockerfile
```

-	Layers:
	-	`sha256:95c2a060b0815de5e11bb9fd7bd737a4ad7667598b7e22d92e35c4f8ac05e996`  
		Last Modified: Wed, 08 May 2024 02:02:59 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c9fe20d7cfa9fbd00b6439168f2651bfda07ffbf00cbadec6d33b9f2f7788`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-enterprise`

```console
$ docker pull neo4j@sha256:8552defe4b2f5325389337291f1afc7e47caa19e371d44f76d934da92e87ca23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise` - linux; amd64

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

### `neo4j:5.19.0-enterprise` - unknown; unknown

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
$ docker pull neo4j@sha256:8552defe4b2f5325389337291f1afc7e47caa19e371d44f76d934da92e87ca23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-bullseye` - linux; amd64

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

### `neo4j:5.19.0-enterprise-bullseye` - unknown; unknown

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
$ docker pull neo4j@sha256:cd4375dca32fdd8484fcfa93b7074b3aa42e490d413e21ed5296b7eee1776895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:696b1068794b2f69e3ed264a9ac5dc631f441358891d926a2519228de6d4cfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.9 MB (572889686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae32533ac43845337108943452af4ea00c706fb0f9212c36bd4d219ed1b511`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98735785b25cc20b3c023ddb1bda8b3d2989ef8ccca7f146055e478cc25ca41`  
		Last Modified: Fri, 10 May 2024 18:52:11 GMT  
		Size: 152.3 MB (152305137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0dcd874afd2fb773e8f9a7b71be53436223e3b6319bd4288218758b2ed802`  
		Last Modified: Fri, 10 May 2024 18:52:09 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12bcb4da80bea0eaec8659de89316cdb885c7b1d0298436b229e6318cfc78f1`  
		Last Modified: Fri, 10 May 2024 18:52:16 GMT  
		Size: 381.3 MB (381284032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:678d61b655e61bd335dbbd557f1fbed392850856d7995401ead0c80a9edcbf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e976e5c2c0c3e556a2f1cc1bc212393dcbfd7caca671f1d2c010c293d7567a26`

```dockerfile
```

-	Layers:
	-	`sha256:01be8535193e29b9f22377f2281b32edbb09f7e13e72a61120b742508899232c`  
		Last Modified: Fri, 10 May 2024 18:52:10 GMT  
		Size: 10.5 MB (10475974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53004001571e0cb476b680e6f7d8b602305b23f76a9ca9e505237802fd32500f`  
		Last Modified: Fri, 10 May 2024 18:52:10 GMT  
		Size: 20.5 KB (20462 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0787c0261a75dfc6cf0dcca7c91d065cdbddf9dbb5a0881529fdc0ba1df37301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569929600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587c79223d4802351010c078db542011a0f857600271cfd3c3faef74aea491fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb64181e0a6ee5bc4621f7fdcbc258f924a917ed5d78ea57a8efec65e186e129`  
		Last Modified: Fri, 10 May 2024 19:18:59 GMT  
		Size: 381.3 MB (381284078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:74eed8a6dc09311522cc523213450983f04e5ada8ebd962b1e7cd36e3914d342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10493817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8872159f066f8956a53d2b389ab74a8947ceeb6946c1b70bf55f1288b7982b79`

```dockerfile
```

-	Layers:
	-	`sha256:a072da0a949c8ba0ad7444b31d957bfae35268f566e7570c7a73cbdb916f3639`  
		Last Modified: Fri, 10 May 2024 19:18:51 GMT  
		Size: 10.5 MB (10473512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76263e58119d5ff9c20eabc9518ba1b15296d52f736f4fc3511ea26862775d9f`  
		Last Modified: Fri, 10 May 2024 19:18:51 GMT  
		Size: 20.3 KB (20305 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9bbcdea01c7b63562da85fb584f62445cb005811a4f773c75ad766aefac94cd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f434c90126e5d2d9ad427e92d7def7d66fa3210c0634f6c6d870ecae702d894a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545909296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb21f9996d62f68c301cf67f2c65d2846a02f034eefe98d9bfee433b227470ea`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3e9d41866091c413f654fc0a05860615b6cddb3817a9ddf4dade67c9e2db7d`  
		Last Modified: Tue, 07 May 2024 21:52:00 GMT  
		Size: 125.7 MB (125729524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304dd60691526542f62607860ee0db40205ea0007d57d0f1457269d1685e76d2`  
		Last Modified: Tue, 07 May 2024 21:51:58 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc51647b3ed161fa625b6c5cda4256f557d40d0ad88ff354056c12f3e15c53bc`  
		Last Modified: Tue, 07 May 2024 21:52:06 GMT  
		Size: 381.3 MB (381283472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4f019b5bb9842c7280e908682599805518af587136b5d7904cc8048d5cc7e529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa465633e4ea0e48642d98ff034836d18e598504c8b70de20b76e41263babb4`

```dockerfile
```

-	Layers:
	-	`sha256:34f7842f0f7dbb9c6ca9de88189cb5b046da2a2f2a61c873fc7bc1f9edb392db`  
		Last Modified: Tue, 07 May 2024 21:51:59 GMT  
		Size: 5.6 MB (5596528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d154c8e4bc881ead54c113d154c30988ce755864b9e90768c0ed77da9f22887`  
		Last Modified: Tue, 07 May 2024 21:51:58 GMT  
		Size: 20.5 KB (20487 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:30f88d0bde554988f0c6c217b8d3c75be4ccc9f2f55bbd7d6a0156809de18940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544129909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60da0bc7666725dee1fd0e6af7117094ef3947ce4c75525c161d5e7a71504867`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a11ba6639e442879d41beacbb496c2919dc04ff18ca854dcd17834055438808`  
		Last Modified: Wed, 08 May 2024 02:38:50 GMT  
		Size: 381.3 MB (381283655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b95009a30fb15d5015406216050c3ad162eb301c295e17b822331a3a46080b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5589831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29238932960c90597d898ea9120e5476fbcea84460982649a7c34c819ccce25`

```dockerfile
```

-	Layers:
	-	`sha256:ebfbb9a45c8f3110a5c6012ba4f90839eaf09c66bcb997471286f50aa7d9f89d`  
		Last Modified: Wed, 08 May 2024 02:38:43 GMT  
		Size: 5.6 MB (5569500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f647e6b7352660a6fa6c0413da7ef6f10128dbdc5091b48028f3e07a77bee77`  
		Last Modified: Wed, 08 May 2024 02:38:42 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-ubi8`

```console
$ docker pull neo4j@sha256:e23e34f9896590da03904aab954edb6d821c95b8511c06952a2d8f698de42c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:cff54c32b9b96e08d1d0b5dbb5f6490ac6e0e88902df64d9f30371108e199df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98145555cd08f53fe064fc227ac2ab3c96dc928d6657cbb27bc7d47070b5ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214bad9fa2f0fbd9a87ce5a23845cd04f89f4e86961aac8acd64a58dbe30b07`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 152.3 MB (152305645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b2eca8bc53ccdaab4b9ab7630b460cc954cf7ffb71032e216713d480f03cf`  
		Last Modified: Fri, 10 May 2024 18:52:03 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f004ce17c2711163aa4dccc17ff88d46e8cdc9fbc023d1cadcd53eee9acd6fb`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 122.8 MB (122827183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:067a39758bc6681c95806007ba09712782f16589dc8d464b60a69cc970fca60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a37c28eb797dcbf15a37e86b6e807c740d382b377b077c9c871bb2b07aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:78cd8ee210804509043c19674c3c534b158201d3475416a621d6aa660fd88e27`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 10.3 MB (10306841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056a2250cdef3123d1991d52063d48244dc9ffbdce9464c7c1f12515ae4232ab`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-ubi9`

```console
$ docker pull neo4j@sha256:ca2fbd072605f1e11c4a2bf7255993d7fca17375a849a11273083ba2d03a3c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c581706f1e6805e4ae0b9935e0c043f589e3760d99f631dc676094d5f2234021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287452952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118790adc66481a526e9b265d1a2e8c91cc151754e69952cef6f92852166734`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53976c770d79e6e3138db213e11cfe0086c4477ef0b1d7634595540cfc6e6b68`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 125.7 MB (125729612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573c66f11ba008460aeb70413941404cd1c3d56c60aff4fdfa89b3289cdc029`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca36784ab94d19d0fbae65461337e24b35ff2bb1f4f35c9c7d71bba918dcec1`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 122.8 MB (122827037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:79a931143aa0f9c6d26372bf483515e4b5069748f5f73a433356bd52ba72964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d0f6120b4e7153fbdbc0f3f875e3c16c6203a6ffb9e4add1e1964f0ccdf20`

```dockerfile
```

-	Layers:
	-	`sha256:0e2db2e554b686f53b839594c05a93a8320d063208d56e01c6414372e6fb48e3`  
		Last Modified: Tue, 07 May 2024 21:52:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea6a2f7274e247e814c49afe2132b83c36742235783e71391ed1766cb968209`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02af71e50a215ff6633db917db2c0b4bae54000d5770988f08cc68e2b078d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43023c34a2aadd531e4c000d6addf90fd608a11d26b8174ffa82ed471d70472`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8723f7f09ed20f0ed179310b9ae5849e8e613e8784a81a22b9456410507166`  
		Last Modified: Wed, 08 May 2024 02:03:01 GMT  
		Size: 122.8 MB (122827004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:72eb84817ce787bc4485c8e188f950c380ee56ac9dd620ee2f6513f4175ced87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ee49faec0f84760062cf258edcae05e956fb58861e35695c83b82a0cb1270d`

```dockerfile
```

-	Layers:
	-	`sha256:95c2a060b0815de5e11bb9fd7bd737a4ad7667598b7e22d92e35c4f8ac05e996`  
		Last Modified: Wed, 08 May 2024 02:02:59 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c9fe20d7cfa9fbd00b6439168f2651bfda07ffbf00cbadec6d33b9f2f7788`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:e23e34f9896590da03904aab954edb6d821c95b8511c06952a2d8f698de42c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:cff54c32b9b96e08d1d0b5dbb5f6490ac6e0e88902df64d9f30371108e199df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98145555cd08f53fe064fc227ac2ab3c96dc928d6657cbb27bc7d47070b5ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214bad9fa2f0fbd9a87ce5a23845cd04f89f4e86961aac8acd64a58dbe30b07`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 152.3 MB (152305645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b2eca8bc53ccdaab4b9ab7630b460cc954cf7ffb71032e216713d480f03cf`  
		Last Modified: Fri, 10 May 2024 18:52:03 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f004ce17c2711163aa4dccc17ff88d46e8cdc9fbc023d1cadcd53eee9acd6fb`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 122.8 MB (122827183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:067a39758bc6681c95806007ba09712782f16589dc8d464b60a69cc970fca60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a37c28eb797dcbf15a37e86b6e807c740d382b377b077c9c871bb2b07aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:78cd8ee210804509043c19674c3c534b158201d3475416a621d6aa660fd88e27`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 10.3 MB (10306841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056a2250cdef3123d1991d52063d48244dc9ffbdce9464c7c1f12515ae4232ab`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:ca2fbd072605f1e11c4a2bf7255993d7fca17375a849a11273083ba2d03a3c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c581706f1e6805e4ae0b9935e0c043f589e3760d99f631dc676094d5f2234021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287452952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118790adc66481a526e9b265d1a2e8c91cc151754e69952cef6f92852166734`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53976c770d79e6e3138db213e11cfe0086c4477ef0b1d7634595540cfc6e6b68`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 125.7 MB (125729612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573c66f11ba008460aeb70413941404cd1c3d56c60aff4fdfa89b3289cdc029`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca36784ab94d19d0fbae65461337e24b35ff2bb1f4f35c9c7d71bba918dcec1`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 122.8 MB (122827037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:79a931143aa0f9c6d26372bf483515e4b5069748f5f73a433356bd52ba72964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d0f6120b4e7153fbdbc0f3f875e3c16c6203a6ffb9e4add1e1964f0ccdf20`

```dockerfile
```

-	Layers:
	-	`sha256:0e2db2e554b686f53b839594c05a93a8320d063208d56e01c6414372e6fb48e3`  
		Last Modified: Tue, 07 May 2024 21:52:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea6a2f7274e247e814c49afe2132b83c36742235783e71391ed1766cb968209`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02af71e50a215ff6633db917db2c0b4bae54000d5770988f08cc68e2b078d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43023c34a2aadd531e4c000d6addf90fd608a11d26b8174ffa82ed471d70472`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8723f7f09ed20f0ed179310b9ae5849e8e613e8784a81a22b9456410507166`  
		Last Modified: Wed, 08 May 2024 02:03:01 GMT  
		Size: 122.8 MB (122827004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:72eb84817ce787bc4485c8e188f950c380ee56ac9dd620ee2f6513f4175ced87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ee49faec0f84760062cf258edcae05e956fb58861e35695c83b82a0cb1270d`

```dockerfile
```

-	Layers:
	-	`sha256:95c2a060b0815de5e11bb9fd7bd737a4ad7667598b7e22d92e35c4f8ac05e996`  
		Last Modified: Wed, 08 May 2024 02:02:59 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c9fe20d7cfa9fbd00b6439168f2651bfda07ffbf00cbadec6d33b9f2f7788`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

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

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:8552defe4b2f5325389337291f1afc7e47caa19e371d44f76d934da92e87ca23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

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

### `neo4j:enterprise-bullseye` - unknown; unknown

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
$ docker pull neo4j@sha256:cd4375dca32fdd8484fcfa93b7074b3aa42e490d413e21ed5296b7eee1776895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:696b1068794b2f69e3ed264a9ac5dc631f441358891d926a2519228de6d4cfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.9 MB (572889686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae32533ac43845337108943452af4ea00c706fb0f9212c36bd4d219ed1b511`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98735785b25cc20b3c023ddb1bda8b3d2989ef8ccca7f146055e478cc25ca41`  
		Last Modified: Fri, 10 May 2024 18:52:11 GMT  
		Size: 152.3 MB (152305137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0dcd874afd2fb773e8f9a7b71be53436223e3b6319bd4288218758b2ed802`  
		Last Modified: Fri, 10 May 2024 18:52:09 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12bcb4da80bea0eaec8659de89316cdb885c7b1d0298436b229e6318cfc78f1`  
		Last Modified: Fri, 10 May 2024 18:52:16 GMT  
		Size: 381.3 MB (381284032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:678d61b655e61bd335dbbd557f1fbed392850856d7995401ead0c80a9edcbf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e976e5c2c0c3e556a2f1cc1bc212393dcbfd7caca671f1d2c010c293d7567a26`

```dockerfile
```

-	Layers:
	-	`sha256:01be8535193e29b9f22377f2281b32edbb09f7e13e72a61120b742508899232c`  
		Last Modified: Fri, 10 May 2024 18:52:10 GMT  
		Size: 10.5 MB (10475974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53004001571e0cb476b680e6f7d8b602305b23f76a9ca9e505237802fd32500f`  
		Last Modified: Fri, 10 May 2024 18:52:10 GMT  
		Size: 20.5 KB (20462 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0787c0261a75dfc6cf0dcca7c91d065cdbddf9dbb5a0881529fdc0ba1df37301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569929600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587c79223d4802351010c078db542011a0f857600271cfd3c3faef74aea491fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb64181e0a6ee5bc4621f7fdcbc258f924a917ed5d78ea57a8efec65e186e129`  
		Last Modified: Fri, 10 May 2024 19:18:59 GMT  
		Size: 381.3 MB (381284078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:74eed8a6dc09311522cc523213450983f04e5ada8ebd962b1e7cd36e3914d342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10493817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8872159f066f8956a53d2b389ab74a8947ceeb6946c1b70bf55f1288b7982b79`

```dockerfile
```

-	Layers:
	-	`sha256:a072da0a949c8ba0ad7444b31d957bfae35268f566e7570c7a73cbdb916f3639`  
		Last Modified: Fri, 10 May 2024 19:18:51 GMT  
		Size: 10.5 MB (10473512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76263e58119d5ff9c20eabc9518ba1b15296d52f736f4fc3511ea26862775d9f`  
		Last Modified: Fri, 10 May 2024 19:18:51 GMT  
		Size: 20.3 KB (20305 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9bbcdea01c7b63562da85fb584f62445cb005811a4f773c75ad766aefac94cd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f434c90126e5d2d9ad427e92d7def7d66fa3210c0634f6c6d870ecae702d894a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.9 MB (545909296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb21f9996d62f68c301cf67f2c65d2846a02f034eefe98d9bfee433b227470ea`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3e9d41866091c413f654fc0a05860615b6cddb3817a9ddf4dade67c9e2db7d`  
		Last Modified: Tue, 07 May 2024 21:52:00 GMT  
		Size: 125.7 MB (125729524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304dd60691526542f62607860ee0db40205ea0007d57d0f1457269d1685e76d2`  
		Last Modified: Tue, 07 May 2024 21:51:58 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc51647b3ed161fa625b6c5cda4256f557d40d0ad88ff354056c12f3e15c53bc`  
		Last Modified: Tue, 07 May 2024 21:52:06 GMT  
		Size: 381.3 MB (381283472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4f019b5bb9842c7280e908682599805518af587136b5d7904cc8048d5cc7e529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa465633e4ea0e48642d98ff034836d18e598504c8b70de20b76e41263babb4`

```dockerfile
```

-	Layers:
	-	`sha256:34f7842f0f7dbb9c6ca9de88189cb5b046da2a2f2a61c873fc7bc1f9edb392db`  
		Last Modified: Tue, 07 May 2024 21:51:59 GMT  
		Size: 5.6 MB (5596528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d154c8e4bc881ead54c113d154c30988ce755864b9e90768c0ed77da9f22887`  
		Last Modified: Tue, 07 May 2024 21:51:58 GMT  
		Size: 20.5 KB (20487 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:30f88d0bde554988f0c6c217b8d3c75be4ccc9f2f55bbd7d6a0156809de18940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544129909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60da0bc7666725dee1fd0e6af7117094ef3947ce4c75525c161d5e7a71504867`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a11ba6639e442879d41beacbb496c2919dc04ff18ca854dcd17834055438808`  
		Last Modified: Wed, 08 May 2024 02:38:50 GMT  
		Size: 381.3 MB (381283655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b95009a30fb15d5015406216050c3ad162eb301c295e17b822331a3a46080b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5589831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29238932960c90597d898ea9120e5476fbcea84460982649a7c34c819ccce25`

```dockerfile
```

-	Layers:
	-	`sha256:ebfbb9a45c8f3110a5c6012ba4f90839eaf09c66bcb997471286f50aa7d9f89d`  
		Last Modified: Wed, 08 May 2024 02:38:43 GMT  
		Size: 5.6 MB (5569500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f647e6b7352660a6fa6c0413da7ef6f10128dbdc5091b48028f3e07a77bee77`  
		Last Modified: Wed, 08 May 2024 02:38:42 GMT  
		Size: 20.3 KB (20331 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:ca735501d082b0b78e7efca4478b1cccfb8b5650c7326f72d218ab9c12fe439c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:828a1263d60f63b2a865083544474ac1262e8da676adfc22de4ac29317067f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302302553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4557205bfb9ff744d1712a336b60a93288f7bea1012eed1c08e67594b105bc37`
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60102e62972bf6a4286bdb091e94ca4243fca91fffb7a8675d7b7268140377bb`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae9d34c647054aa0ce8c0e3d76aa14da54a55562dd3857c2e06f1c62f378b2`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e51257b6e3b74d378ed5a78aa61b6a6e1563dba7e77f86e2d4eb9a9eb67cd`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25314bf5932f28edb113613b884062dfc3f5d59794fe2aab819426deecbc293f`  
		Last Modified: Tue, 14 May 2024 02:56:42 GMT  
		Size: 125.8 MB (125760170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:b687857292b399141dc295f57c267042b270f9af79be37c583e3723ae7568646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bfed4ebb07563f4816c25c3d4c043783623d96f9b6317f4ed899f13d7a442`

```dockerfile
```

-	Layers:
	-	`sha256:1cb1d16943809d1cc93ee24890778e732bd9ec33f1e3173b5b8ec86db48ff7af`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 3.0 MB (2959711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0136379b3eee311caef0a80216c9c1d5efcbca8ee3702a448f92da47948b1e1`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
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
$ docker pull neo4j@sha256:e23e34f9896590da03904aab954edb6d821c95b8511c06952a2d8f698de42c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:cff54c32b9b96e08d1d0b5dbb5f6490ac6e0e88902df64d9f30371108e199df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98145555cd08f53fe064fc227ac2ab3c96dc928d6657cbb27bc7d47070b5ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:312a52fb00fdcfe4be678f55fd46bd7e8ce77b2e7562f624009d4f0f6ba6f923 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:d63810d9cb650af2bfebdbec17878db280f6a934d579f00e0c0cc4f3fd257e89 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:08e2a9c3fee04ea7c287ffee653be9f64e52f17e25f95ea339cf15cebf1e050f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:ca19c1d8b6a56d82b4d9cc9ee30899ce07641f8ba17831ffd074240384f32cb0`  
		Last Modified: Wed, 08 May 2024 18:29:43 GMT  
		Size: 39.3 MB (39290787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214bad9fa2f0fbd9a87ce5a23845cd04f89f4e86961aac8acd64a58dbe30b07`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 152.3 MB (152305645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b2eca8bc53ccdaab4b9ab7630b460cc954cf7ffb71032e216713d480f03cf`  
		Last Modified: Fri, 10 May 2024 18:52:03 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f004ce17c2711163aa4dccc17ff88d46e8cdc9fbc023d1cadcd53eee9acd6fb`  
		Last Modified: Fri, 10 May 2024 18:52:07 GMT  
		Size: 122.8 MB (122827183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:067a39758bc6681c95806007ba09712782f16589dc8d464b60a69cc970fca60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10328481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a37c28eb797dcbf15a37e86b6e807c740d382b377b077c9c871bb2b07aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:78cd8ee210804509043c19674c3c534b158201d3475416a621d6aa660fd88e27`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 10.3 MB (10306841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056a2250cdef3123d1991d52063d48244dc9ffbdce9464c7c1f12515ae4232ab`  
		Last Modified: Fri, 10 May 2024 18:52:04 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:ca2fbd072605f1e11c4a2bf7255993d7fca17375a849a11273083ba2d03a3c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c581706f1e6805e4ae0b9935e0c043f589e3760d99f631dc676094d5f2234021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287452952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118790adc66481a526e9b265d1a2e8c91cc151754e69952cef6f92852166734`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53976c770d79e6e3138db213e11cfe0086c4477ef0b1d7634595540cfc6e6b68`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 125.7 MB (125729612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573c66f11ba008460aeb70413941404cd1c3d56c60aff4fdfa89b3289cdc029`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca36784ab94d19d0fbae65461337e24b35ff2bb1f4f35c9c7d71bba918dcec1`  
		Last Modified: Tue, 07 May 2024 21:52:07 GMT  
		Size: 122.8 MB (122827037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:79a931143aa0f9c6d26372bf483515e4b5069748f5f73a433356bd52ba72964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d0f6120b4e7153fbdbc0f3f875e3c16c6203a6ffb9e4add1e1964f0ccdf20`

```dockerfile
```

-	Layers:
	-	`sha256:0e2db2e554b686f53b839594c05a93a8320d063208d56e01c6414372e6fb48e3`  
		Last Modified: Tue, 07 May 2024 21:52:05 GMT  
		Size: 5.4 MB (5427395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea6a2f7274e247e814c49afe2132b83c36742235783e71391ed1766cb968209`  
		Last Modified: Tue, 07 May 2024 21:52:04 GMT  
		Size: 21.7 KB (21666 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02af71e50a215ff6633db917db2c0b4bae54000d5770988f08cc68e2b078d509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43023c34a2aadd531e4c000d6addf90fd608a11d26b8174ffa82ed471d70472`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
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
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4995d0d6f5426864002a2ece65e4121917d5aa5133eb763741ba2e0b9bfd0`  
		Last Modified: Wed, 08 May 2024 02:03:02 GMT  
		Size: 125.7 MB (125745882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf74da74cc58771e4bf48d4512fc23ef5fd6ea2ac7b9fa8faca1f39fc1fee4`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8723f7f09ed20f0ed179310b9ae5849e8e613e8784a81a22b9456410507166`  
		Last Modified: Wed, 08 May 2024 02:03:01 GMT  
		Size: 122.8 MB (122827004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:72eb84817ce787bc4485c8e188f950c380ee56ac9dd620ee2f6513f4175ced87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ee49faec0f84760062cf258edcae05e956fb58861e35695c83b82a0cb1270d`

```dockerfile
```

-	Layers:
	-	`sha256:95c2a060b0815de5e11bb9fd7bd737a4ad7667598b7e22d92e35c4f8ac05e996`  
		Last Modified: Wed, 08 May 2024 02:02:59 GMT  
		Size: 5.4 MB (5400375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298c9fe20d7cfa9fbd00b6439168f2651bfda07ffbf00cbadec6d33b9f2f7788`  
		Last Modified: Wed, 08 May 2024 02:02:58 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json
