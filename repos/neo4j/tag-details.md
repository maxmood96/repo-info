<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.38`](#neo4j4438)
-	[`neo4j:4.4.38-community`](#neo4j4438-community)
-	[`neo4j:4.4.38-enterprise`](#neo4j4438-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi9`](#neo4j5-community-ubi9)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi9`](#neo4j5-enterprise-ubi9)
-	[`neo4j:5-ubi9`](#neo4j5-ubi9)
-	[`neo4j:5.24`](#neo4j524)
-	[`neo4j:5.24-bullseye`](#neo4j524-bullseye)
-	[`neo4j:5.24-community`](#neo4j524-community)
-	[`neo4j:5.24-community-bullseye`](#neo4j524-community-bullseye)
-	[`neo4j:5.24-community-ubi9`](#neo4j524-community-ubi9)
-	[`neo4j:5.24-enterprise`](#neo4j524-enterprise)
-	[`neo4j:5.24-enterprise-bullseye`](#neo4j524-enterprise-bullseye)
-	[`neo4j:5.24-enterprise-ubi9`](#neo4j524-enterprise-ubi9)
-	[`neo4j:5.24-ubi9`](#neo4j524-ubi9)
-	[`neo4j:5.24.2`](#neo4j5242)
-	[`neo4j:5.24.2-bullseye`](#neo4j5242-bullseye)
-	[`neo4j:5.24.2-community`](#neo4j5242-community)
-	[`neo4j:5.24.2-community-bullseye`](#neo4j5242-community-bullseye)
-	[`neo4j:5.24.2-community-ubi9`](#neo4j5242-community-ubi9)
-	[`neo4j:5.24.2-enterprise`](#neo4j5242-enterprise)
-	[`neo4j:5.24.2-enterprise-bullseye`](#neo4j5242-enterprise-bullseye)
-	[`neo4j:5.24.2-enterprise-ubi9`](#neo4j5242-enterprise-ubi9)
-	[`neo4j:5.24.2-ubi9`](#neo4j5242-ubi9)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi9`](#neo4jcommunity-ubi9)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi9`](#neo4jenterprise-ubi9)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi9`](#neo4jubi9)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:b6cd41b576fa5da104b241e0e91548515b255ff1feb75cc79b09ca1201403714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:c2ad977e4605d101baa4f488b342eb76551fb700aedf0dfe5e5c33f7dd4f7324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306081223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f22662f10ade8b15a19f38a39ba2840b8a3dbf485ff8619ae73e029b7d9af7e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ee45879de6d5549a46c474daa721d5d2ceb92e11536f3852d95d527b5eed8`  
		Last Modified: Sat, 12 Oct 2024 00:55:24 GMT  
		Size: 145.5 MB (145549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c645f475c25a35da90f50a48f5de464835f1046546b488f5db3e2de18ca7b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dde6c0a7f05f9f90416b7d5596e132cfb2b93ad50221538469c3c8675c315fa`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6482869e81d5a4578d291f476ac18a45fe83407eee173ce3a723bbd8b728c59a`  
		Last Modified: Sat, 12 Oct 2024 00:55:23 GMT  
		Size: 129.1 MB (129088889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:e17b00028301a0b0e240be6dcac6d87ac5d9e4e86ecad124d8af6883ef999065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a1f8aaa35658875455899d6b0c4438c2c2af2903121424bd287cfd2be8aa29`

```dockerfile
```

-	Layers:
	-	`sha256:1dd4baf415638c01968dba518d9e06c2b2d59f5ee3cbcce0800e7ba195a062d2`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1319996d485c5683c3813f7c2fc25344db01c0b8acee848a84a25c026e8f2c54`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d7b24906d93071c08f65e9311b8b1c7245ee20b927a84372c77ce615659436e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301496880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62749f92550bd3e79a64fbccfdbee3efc9b29db4587270b18b4a45630b22434`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33771f245d60b4ba877a7fcdcfef422da7796464ee121d48fd7a3fa7b21189d`  
		Last Modified: Sat, 12 Oct 2024 01:07:47 GMT  
		Size: 142.4 MB (142355083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c02891b2136db5a0387128ddde1a9ed242b881e81840f637b21b09f73ec530d`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd04fddac271a13af76c0361e9e3cc41262b3f37cb82add906ade5a5bccbb4b`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bdc20697f2acee118e5abe5a74011fbf1bbee13fb2610f382fb7b9c010765c`  
		Last Modified: Sat, 12 Oct 2024 01:57:37 GMT  
		Size: 129.1 MB (129052774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:78d1a6f593948cbe74be229e25fed3f999c411c740c1480708c2f71745406004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d831b7d3474c0e23729cd417c249a363e43cff66c802ecb70805f0c01e4a5`

```dockerfile
```

-	Layers:
	-	`sha256:dc4eec78d08a6eff0d19b4382e36f451b55098926722d3a98e654ea450b5232e`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94b43a1cb2b64adf0b390f6c384782e9f0d2d161893dac9426260af5b0e3ef5`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 19.8 KB (19762 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:b6cd41b576fa5da104b241e0e91548515b255ff1feb75cc79b09ca1201403714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:c2ad977e4605d101baa4f488b342eb76551fb700aedf0dfe5e5c33f7dd4f7324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306081223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f22662f10ade8b15a19f38a39ba2840b8a3dbf485ff8619ae73e029b7d9af7e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ee45879de6d5549a46c474daa721d5d2ceb92e11536f3852d95d527b5eed8`  
		Last Modified: Sat, 12 Oct 2024 00:55:24 GMT  
		Size: 145.5 MB (145549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c645f475c25a35da90f50a48f5de464835f1046546b488f5db3e2de18ca7b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dde6c0a7f05f9f90416b7d5596e132cfb2b93ad50221538469c3c8675c315fa`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6482869e81d5a4578d291f476ac18a45fe83407eee173ce3a723bbd8b728c59a`  
		Last Modified: Sat, 12 Oct 2024 00:55:23 GMT  
		Size: 129.1 MB (129088889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e17b00028301a0b0e240be6dcac6d87ac5d9e4e86ecad124d8af6883ef999065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a1f8aaa35658875455899d6b0c4438c2c2af2903121424bd287cfd2be8aa29`

```dockerfile
```

-	Layers:
	-	`sha256:1dd4baf415638c01968dba518d9e06c2b2d59f5ee3cbcce0800e7ba195a062d2`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1319996d485c5683c3813f7c2fc25344db01c0b8acee848a84a25c026e8f2c54`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d7b24906d93071c08f65e9311b8b1c7245ee20b927a84372c77ce615659436e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301496880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62749f92550bd3e79a64fbccfdbee3efc9b29db4587270b18b4a45630b22434`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33771f245d60b4ba877a7fcdcfef422da7796464ee121d48fd7a3fa7b21189d`  
		Last Modified: Sat, 12 Oct 2024 01:07:47 GMT  
		Size: 142.4 MB (142355083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c02891b2136db5a0387128ddde1a9ed242b881e81840f637b21b09f73ec530d`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd04fddac271a13af76c0361e9e3cc41262b3f37cb82add906ade5a5bccbb4b`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bdc20697f2acee118e5abe5a74011fbf1bbee13fb2610f382fb7b9c010765c`  
		Last Modified: Sat, 12 Oct 2024 01:57:37 GMT  
		Size: 129.1 MB (129052774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:78d1a6f593948cbe74be229e25fed3f999c411c740c1480708c2f71745406004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d831b7d3474c0e23729cd417c249a363e43cff66c802ecb70805f0c01e4a5`

```dockerfile
```

-	Layers:
	-	`sha256:dc4eec78d08a6eff0d19b4382e36f451b55098926722d3a98e654ea450b5232e`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94b43a1cb2b64adf0b390f6c384782e9f0d2d161893dac9426260af5b0e3ef5`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 19.8 KB (19762 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:d109fb47142e3b4c1af101b165af3e34bd1aa31cc4206d851634764086a27d5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:74cc7cfb2d6f339cba4a77568298b8c9bcb4085f3d04662ef38143d746378801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.5 MB (410487598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2549c4301b19b36680c0d2355ec1cd4d0e2473f29cbc2067a78b8a398acffbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ab9fe6a9bd6c76d679070597d7129e68bbc9a3be473b6b07bd68e852026e54f0 NEO4J_TARBALL=neo4j-enterprise-4.4.38-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d65da1ea3f89fb4831e0ee2d6d28d29b6909b941d9dba807a4167067eba3f`  
		Last Modified: Sat, 12 Oct 2024 00:55:29 GMT  
		Size: 145.5 MB (145549901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c0aed24da0cd018bce43f2c93cd96ecd82e5cb3467d6c1297698e5a13edda`  
		Last Modified: Sat, 12 Oct 2024 00:55:26 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973942ddc708e1e36618901ab2f25fcfd4f88bc24d108f35e974afd5afa658eb`  
		Last Modified: Sat, 12 Oct 2024 00:55:30 GMT  
		Size: 233.5 MB (233495260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ebda63d7d0e4e6e26c0462f945ed41661ece43d2ad60df9d516f0ba3cba263e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3319649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3116f45a01b27046c0cc04451aea73a9bfcbe5af57582e09c1516bd00e3f80`

```dockerfile
```

-	Layers:
	-	`sha256:30c18927eb69087d69e9bd9696345ce4d065955803b06128a21c47b5345e986f`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.3 MB (3300589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d197a14af075abec77964b39954cf7e125ae16b69a7b069461817d870e8eac`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8ac7401a84c5303bd3a4011ca63be294abad36f337c4c0d0cc08e4650ac0e8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.9 MB (405906957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0312b42499d3e7748ab0505fb4f690e14f0b7d76aa0a45cbfd16641bc71d2beb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ab9fe6a9bd6c76d679070597d7129e68bbc9a3be473b6b07bd68e852026e54f0 NEO4J_TARBALL=neo4j-enterprise-4.4.38-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33771f245d60b4ba877a7fcdcfef422da7796464ee121d48fd7a3fa7b21189d`  
		Last Modified: Sat, 12 Oct 2024 01:07:47 GMT  
		Size: 142.4 MB (142355083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f2024a7039e9ec25b972ce09e9ab121594a68f36a61d15ac2c4ed697725034`  
		Last Modified: Sat, 12 Oct 2024 01:58:53 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbe48d254ac59df06bd8bde5d48a709ac6740753139b21591b8a793e5b90ac`  
		Last Modified: Sat, 12 Oct 2024 01:58:53 GMT  
		Size: 10.0 KB (9956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f946dc37ee2660556ac5bf0ac5b6e3c53e56d14426b38ba4c4ba5b7adcce10`  
		Last Modified: Sat, 12 Oct 2024 01:58:58 GMT  
		Size: 233.5 MB (233462855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:d23805e4a83b29a06972f00d3f7b47957f3b7bee6cb8873fdb2beb78e108e430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3319997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dfb063a7624b45aa4f1e9ac16a959477dc1f319376657f660685a605910675`

```dockerfile
```

-	Layers:
	-	`sha256:cd93f78d3f88494681128c2d28601b8731a66d8eaeed796d700b1eb80ff3f0bd`  
		Last Modified: Sat, 12 Oct 2024 01:58:53 GMT  
		Size: 3.3 MB (3300828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edbc8f4a82f4b0065a191871f29d53b100d3d759f4ce0605c2ab49a4316c49b`  
		Last Modified: Sat, 12 Oct 2024 01:58:53 GMT  
		Size: 19.2 KB (19169 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.38`

```console
$ docker pull neo4j@sha256:b6cd41b576fa5da104b241e0e91548515b255ff1feb75cc79b09ca1201403714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.38` - linux; amd64

```console
$ docker pull neo4j@sha256:c2ad977e4605d101baa4f488b342eb76551fb700aedf0dfe5e5c33f7dd4f7324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306081223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f22662f10ade8b15a19f38a39ba2840b8a3dbf485ff8619ae73e029b7d9af7e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ee45879de6d5549a46c474daa721d5d2ceb92e11536f3852d95d527b5eed8`  
		Last Modified: Sat, 12 Oct 2024 00:55:24 GMT  
		Size: 145.5 MB (145549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c645f475c25a35da90f50a48f5de464835f1046546b488f5db3e2de18ca7b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dde6c0a7f05f9f90416b7d5596e132cfb2b93ad50221538469c3c8675c315fa`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6482869e81d5a4578d291f476ac18a45fe83407eee173ce3a723bbd8b728c59a`  
		Last Modified: Sat, 12 Oct 2024 00:55:23 GMT  
		Size: 129.1 MB (129088889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38` - unknown; unknown

```console
$ docker pull neo4j@sha256:e17b00028301a0b0e240be6dcac6d87ac5d9e4e86ecad124d8af6883ef999065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a1f8aaa35658875455899d6b0c4438c2c2af2903121424bd287cfd2be8aa29`

```dockerfile
```

-	Layers:
	-	`sha256:1dd4baf415638c01968dba518d9e06c2b2d59f5ee3cbcce0800e7ba195a062d2`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1319996d485c5683c3813f7c2fc25344db01c0b8acee848a84a25c026e8f2c54`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.38` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d7b24906d93071c08f65e9311b8b1c7245ee20b927a84372c77ce615659436e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301496880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62749f92550bd3e79a64fbccfdbee3efc9b29db4587270b18b4a45630b22434`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33771f245d60b4ba877a7fcdcfef422da7796464ee121d48fd7a3fa7b21189d`  
		Last Modified: Sat, 12 Oct 2024 01:07:47 GMT  
		Size: 142.4 MB (142355083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c02891b2136db5a0387128ddde1a9ed242b881e81840f637b21b09f73ec530d`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd04fddac271a13af76c0361e9e3cc41262b3f37cb82add906ade5a5bccbb4b`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bdc20697f2acee118e5abe5a74011fbf1bbee13fb2610f382fb7b9c010765c`  
		Last Modified: Sat, 12 Oct 2024 01:57:37 GMT  
		Size: 129.1 MB (129052774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38` - unknown; unknown

```console
$ docker pull neo4j@sha256:78d1a6f593948cbe74be229e25fed3f999c411c740c1480708c2f71745406004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d831b7d3474c0e23729cd417c249a363e43cff66c802ecb70805f0c01e4a5`

```dockerfile
```

-	Layers:
	-	`sha256:dc4eec78d08a6eff0d19b4382e36f451b55098926722d3a98e654ea450b5232e`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94b43a1cb2b64adf0b390f6c384782e9f0d2d161893dac9426260af5b0e3ef5`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 19.8 KB (19762 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.38-community`

```console
$ docker pull neo4j@sha256:b6cd41b576fa5da104b241e0e91548515b255ff1feb75cc79b09ca1201403714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.38-community` - linux; amd64

```console
$ docker pull neo4j@sha256:c2ad977e4605d101baa4f488b342eb76551fb700aedf0dfe5e5c33f7dd4f7324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306081223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f22662f10ade8b15a19f38a39ba2840b8a3dbf485ff8619ae73e029b7d9af7e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ee45879de6d5549a46c474daa721d5d2ceb92e11536f3852d95d527b5eed8`  
		Last Modified: Sat, 12 Oct 2024 00:55:24 GMT  
		Size: 145.5 MB (145549900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c645f475c25a35da90f50a48f5de464835f1046546b488f5db3e2de18ca7b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dde6c0a7f05f9f90416b7d5596e132cfb2b93ad50221538469c3c8675c315fa`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6482869e81d5a4578d291f476ac18a45fe83407eee173ce3a723bbd8b728c59a`  
		Last Modified: Sat, 12 Oct 2024 00:55:23 GMT  
		Size: 129.1 MB (129088889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e17b00028301a0b0e240be6dcac6d87ac5d9e4e86ecad124d8af6883ef999065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a1f8aaa35658875455899d6b0c4438c2c2af2903121424bd287cfd2be8aa29`

```dockerfile
```

-	Layers:
	-	`sha256:1dd4baf415638c01968dba518d9e06c2b2d59f5ee3cbcce0800e7ba195a062d2`  
		Last Modified: Sat, 12 Oct 2024 00:55:20 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1319996d485c5683c3813f7c2fc25344db01c0b8acee848a84a25c026e8f2c54`  
		Last Modified: Sat, 12 Oct 2024 00:55:19 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.38-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d7b24906d93071c08f65e9311b8b1c7245ee20b927a84372c77ce615659436e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301496880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62749f92550bd3e79a64fbccfdbee3efc9b29db4587270b18b4a45630b22434`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33771f245d60b4ba877a7fcdcfef422da7796464ee121d48fd7a3fa7b21189d`  
		Last Modified: Sat, 12 Oct 2024 01:07:47 GMT  
		Size: 142.4 MB (142355083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c02891b2136db5a0387128ddde1a9ed242b881e81840f637b21b09f73ec530d`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd04fddac271a13af76c0361e9e3cc41262b3f37cb82add906ade5a5bccbb4b`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bdc20697f2acee118e5abe5a74011fbf1bbee13fb2610f382fb7b9c010765c`  
		Last Modified: Sat, 12 Oct 2024 01:57:37 GMT  
		Size: 129.1 MB (129052774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:78d1a6f593948cbe74be229e25fed3f999c411c740c1480708c2f71745406004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d831b7d3474c0e23729cd417c249a363e43cff66c802ecb70805f0c01e4a5`

```dockerfile
```

-	Layers:
	-	`sha256:dc4eec78d08a6eff0d19b4382e36f451b55098926722d3a98e654ea450b5232e`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94b43a1cb2b64adf0b390f6c384782e9f0d2d161893dac9426260af5b0e3ef5`  
		Last Modified: Sat, 12 Oct 2024 01:57:34 GMT  
		Size: 19.8 KB (19762 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.38-enterprise`

```console
$ docker pull neo4j@sha256:d109fb47142e3b4c1af101b165af3e34bd1aa31cc4206d851634764086a27d5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.38-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:74cc7cfb2d6f339cba4a77568298b8c9bcb4085f3d04662ef38143d746378801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.5 MB (410487598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2549c4301b19b36680c0d2355ec1cd4d0e2473f29cbc2067a78b8a398acffbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ab9fe6a9bd6c76d679070597d7129e68bbc9a3be473b6b07bd68e852026e54f0 NEO4J_TARBALL=neo4j-enterprise-4.4.38-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d65da1ea3f89fb4831e0ee2d6d28d29b6909b941d9dba807a4167067eba3f`  
		Last Modified: Sat, 12 Oct 2024 00:55:29 GMT  
		Size: 145.5 MB (145549901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c0aed24da0cd018bce43f2c93cd96ecd82e5cb3467d6c1297698e5a13edda`  
		Last Modified: Sat, 12 Oct 2024 00:55:26 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973942ddc708e1e36618901ab2f25fcfd4f88bc24d108f35e974afd5afa658eb`  
		Last Modified: Sat, 12 Oct 2024 00:55:30 GMT  
		Size: 233.5 MB (233495260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ebda63d7d0e4e6e26c0462f945ed41661ece43d2ad60df9d516f0ba3cba263e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3319649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3116f45a01b27046c0cc04451aea73a9bfcbe5af57582e09c1516bd00e3f80`

```dockerfile
```

-	Layers:
	-	`sha256:30c18927eb69087d69e9bd9696345ce4d065955803b06128a21c47b5345e986f`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.3 MB (3300589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d197a14af075abec77964b39954cf7e125ae16b69a7b069461817d870e8eac`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.38-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8ac7401a84c5303bd3a4011ca63be294abad36f337c4c0d0cc08e4650ac0e8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.9 MB (405906957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0312b42499d3e7748ab0505fb4f690e14f0b7d76aa0a45cbfd16641bc71d2beb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ab9fe6a9bd6c76d679070597d7129e68bbc9a3be473b6b07bd68e852026e54f0 NEO4J_TARBALL=neo4j-enterprise-4.4.38-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33771f245d60b4ba877a7fcdcfef422da7796464ee121d48fd7a3fa7b21189d`  
		Last Modified: Sat, 12 Oct 2024 01:07:47 GMT  
		Size: 142.4 MB (142355083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f2024a7039e9ec25b972ce09e9ab121594a68f36a61d15ac2c4ed697725034`  
		Last Modified: Sat, 12 Oct 2024 01:58:53 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbe48d254ac59df06bd8bde5d48a709ac6740753139b21591b8a793e5b90ac`  
		Last Modified: Sat, 12 Oct 2024 01:58:53 GMT  
		Size: 10.0 KB (9956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f946dc37ee2660556ac5bf0ac5b6e3c53e56d14426b38ba4c4ba5b7adcce10`  
		Last Modified: Sat, 12 Oct 2024 01:58:58 GMT  
		Size: 233.5 MB (233462855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:d23805e4a83b29a06972f00d3f7b47957f3b7bee6cb8873fdb2beb78e108e430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3319997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dfb063a7624b45aa4f1e9ac16a959477dc1f319376657f660685a605910675`

```dockerfile
```

-	Layers:
	-	`sha256:cd93f78d3f88494681128c2d28601b8731a66d8eaeed796d700b1eb80ff3f0bd`  
		Last Modified: Sat, 12 Oct 2024 01:58:53 GMT  
		Size: 3.3 MB (3300828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edbc8f4a82f4b0065a191871f29d53b100d3d759f4ce0605c2ab49a4316c49b`  
		Last Modified: Sat, 12 Oct 2024 01:58:53 GMT  
		Size: 19.2 KB (19169 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:aecd06ae59ffa1ce84272c31aa0cba385bc20ee40694b5fd94563f3107e96700
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:11f8cce84ec751a7d20fca0cd8869e22df8bb3e3d32ef535ba07939ec4fa8e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297982036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a6616c54689264a1d2e6135363fd2c98ac4c79e8543f4ad800a1d91dd219c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8d28d5756fd38a4b3d4cb29bed83b190b30336d4a8d0edae89a92a6bc18785`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 130.5 MB (130471633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3379440813b187578ecb4f2b3737839a7f983df12d22ee11efb811957730712a`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b45dc9a5fd807a802206d70e1cfa2d07c77c4a92a03af0d01965369b2f804a`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 128.4 MB (128398662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:85cfc55c3194b2e4e996a512c90ff90261b4ce5632e45a4d6d92bcc159003d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5596767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a997650cfd9cbf57da31612b46cc0a1a74a7153caa7a2afc6a094c7121208`

```dockerfile
```

-	Layers:
	-	`sha256:1714d8e4ee1853bd2b8e39fa1646979557f9433de6a80f0eab004ccf6f7893a2`  
		Last Modified: Thu, 03 Oct 2024 16:58:23 GMT  
		Size: 5.6 MB (5574999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c64bd46995faa9273d359b075335da3d023bf27c57ccba375ce282e0009a9d`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 21.8 KB (21768 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:80904012ea7f7ecf62b6852b1133cb8fcc78b93cc7d816ce12b8e63b0dce69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295756870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7beb8d486e41da40ece889f83e6f4b75bc6f2630c00297fe3eeee09ba9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e86b65debcab04675289daf0519879958a8b08fdd7f6d3c75e2812f6ab8b5`  
		Last Modified: Wed, 16 Oct 2024 01:35:55 GMT  
		Size: 128.4 MB (128429899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bdc718fa20e132153311b5cb54d7249eeb3bc7c737fcc6111c9ab804b96c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f82734a381690c7ea06cda6e16842718abb9b16cb0d6c26ac7b48d1e51afbb`

```dockerfile
```

-	Layers:
	-	`sha256:3cef2b4c281264da4ef550401c4d2e03c35de852d05e71cfcd46a32d9fda5a27`  
		Last Modified: Wed, 16 Oct 2024 01:35:53 GMT  
		Size: 5.6 MB (5555861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81269aefe8951f03d6e5eac745ace7a473319c8003405930f95a5e9ce8dbf56f`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:0666f8ae5c7d34abf7b20b6e90c4a207d0d362bf6305e1a8dfdff54bcc3c4ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:590c27d5bba2d730565a557a7814fa882a9f15e04c1764cb201eabab9e604eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594431321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72a2667dc06e9e63841b1c356d91f347e325e651cc781bcdd02fc41feed89`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4795283092d21e11e6420af407ae339d038ee0f6e57eff13590d16716114c`  
		Last Modified: Sat, 12 Oct 2024 00:55:41 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e53848ab5f1a212ed1451e202eb7325a4265c9b6aaac6d17b7199b032740`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b411f01df6bc07ae62e8f24d3ca78ff67f63d59140b4c506941d4ee04f045b`  
		Last Modified: Sat, 12 Oct 2024 00:55:44 GMT  
		Size: 417.8 MB (417822283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f183703ddeef3cd31de960d02e0d63ebfb6a09c288771ac5ff7d3dcaa4303d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfe855c2d8e2c85eb0f650e6be7e05309957de9c404fac9c7935fc96237ef2`

```dockerfile
```

-	Layers:
	-	`sha256:c7841d8712194410176ae5e538da763bce05265594ba1741489a587ae6b2841a`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 3.5 MB (3467938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbdf2a9fb713de81bdfd1ceb95b57146364555e4dbda32e86b05fb613ca526f`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0a9a826c3f3b5bbdc0f188d1862f72ad03344b625e61ce627a4a3c8e8f419fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591834754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96b88717f157516a6a72a8f1c99e2d053265b93709f800b6f89b6d6dc6c0981`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b8b2c0c6cbf5bd6f5f098210e2abbdbc8ec35b22022f7c15a1ca516db6497`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5362fc052deffc3962231d660dd131a36f151e07c3f2796d2d2045762cd91f2`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22290c1bb6fe3fb6d51d60ed418901680becc046f0effeded324de024cd5bdb`  
		Last Modified: Sat, 12 Oct 2024 01:56:34 GMT  
		Size: 417.8 MB (417786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2450a25f361d6b8e8413145e18c89ed22c0a149a0fe9b5cfca51edfb2ad3830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2f46402ccc6f78e666f88b8fcf0256ee38942feaa3761d0b1835564992ef54`

```dockerfile
```

-	Layers:
	-	`sha256:855a223e9a1bfe6e68ef987d624a20d21838a7430894da4715eb38ff6b64703b`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.5 MB (3467630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700782de77acf9194d6a3c16de88d92c3ba35c50fdf2ffd2fef5fb5757057a45`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 21.2 KB (21237 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:0666f8ae5c7d34abf7b20b6e90c4a207d0d362bf6305e1a8dfdff54bcc3c4ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:590c27d5bba2d730565a557a7814fa882a9f15e04c1764cb201eabab9e604eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594431321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72a2667dc06e9e63841b1c356d91f347e325e651cc781bcdd02fc41feed89`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4795283092d21e11e6420af407ae339d038ee0f6e57eff13590d16716114c`  
		Last Modified: Sat, 12 Oct 2024 00:55:41 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e53848ab5f1a212ed1451e202eb7325a4265c9b6aaac6d17b7199b032740`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b411f01df6bc07ae62e8f24d3ca78ff67f63d59140b4c506941d4ee04f045b`  
		Last Modified: Sat, 12 Oct 2024 00:55:44 GMT  
		Size: 417.8 MB (417822283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f183703ddeef3cd31de960d02e0d63ebfb6a09c288771ac5ff7d3dcaa4303d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfe855c2d8e2c85eb0f650e6be7e05309957de9c404fac9c7935fc96237ef2`

```dockerfile
```

-	Layers:
	-	`sha256:c7841d8712194410176ae5e538da763bce05265594ba1741489a587ae6b2841a`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 3.5 MB (3467938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbdf2a9fb713de81bdfd1ceb95b57146364555e4dbda32e86b05fb613ca526f`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0a9a826c3f3b5bbdc0f188d1862f72ad03344b625e61ce627a4a3c8e8f419fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591834754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96b88717f157516a6a72a8f1c99e2d053265b93709f800b6f89b6d6dc6c0981`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b8b2c0c6cbf5bd6f5f098210e2abbdbc8ec35b22022f7c15a1ca516db6497`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5362fc052deffc3962231d660dd131a36f151e07c3f2796d2d2045762cd91f2`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22290c1bb6fe3fb6d51d60ed418901680becc046f0effeded324de024cd5bdb`  
		Last Modified: Sat, 12 Oct 2024 01:56:34 GMT  
		Size: 417.8 MB (417786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2450a25f361d6b8e8413145e18c89ed22c0a149a0fe9b5cfca51edfb2ad3830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2f46402ccc6f78e666f88b8fcf0256ee38942feaa3761d0b1835564992ef54`

```dockerfile
```

-	Layers:
	-	`sha256:855a223e9a1bfe6e68ef987d624a20d21838a7430894da4715eb38ff6b64703b`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.5 MB (3467630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700782de77acf9194d6a3c16de88d92c3ba35c50fdf2ffd2fef5fb5757057a45`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 21.2 KB (21237 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:06186ebe260bba187b9232406b0f6512fa2bf6492c43bb4211c01ff63d0fc414
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c5165682e4c3184b98ffa78364e182f6e140d7ba80bc13d1471c33a42936ca4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584476713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75814d862d65790d31cf7452aad9bb4582b322aea1cf53a4c208da73f0f427d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a2667db7626e9689afefaaa859d8c99203a4c5848ab291f86aa7e6ee5652a9`  
		Last Modified: Thu, 03 Oct 2024 16:58:36 GMT  
		Size: 130.5 MB (130471618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd8e20163536ab988cee7f3eb02797ed6dc49269a1aad93bab95dee73b069f4`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 10.0 KB (10008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df727bcd4b740fb7d4ae1f82b2b12e9eebe3432a6c50f5cecb51a636880ded51`  
		Last Modified: Thu, 03 Oct 2024 16:58:40 GMT  
		Size: 414.9 MB (414893355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1b3bb6c78d7b647b520c7dc40464faa4eb456aa0e0feba51887001060fb0180c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5885640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5e321376f7e52ca4cc75752515fb52064e18a51defe09b023c9d2bce65899`

```dockerfile
```

-	Layers:
	-	`sha256:ffa8a0578ce6b7b6b2335553e37d033634b25be3db137ad8f2933613a3dd8849`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 5.9 MB (5865050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0441d0f852989cb183733f03b4969085b83c5b591b902e1bf186b98884e674b`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 20.6 KB (20590 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:304f60f068da68eafe8da73e574cb59db92c25571092ab2bac6c5e1f93b44ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582250395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48eeb41d00ac2c2187f0755fe26096557c659ed4793515c7d6ba628b296dc2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7ce97bd9a4348af14df442f00b3dc5085b5983d6f03da643744838c7a1bc8ba7 NEO4J_TARBALL=neo4j-enterprise-5.24.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf5c8d1888bff8b7e1efdfa99f2e3c6cc5d44ed7273695b14636614f5df1146`  
		Last Modified: Wed, 16 Oct 2024 01:37:15 GMT  
		Size: 414.9 MB (414923424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5fc0196480e8c3bcff8ee15cfd7f0c99c05bc0330b81021887e19eff6a994bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5866600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18754f5534ac8404dcd3b51edfe12611f21787d70f53e57b4e16ce866c338683`

```dockerfile
```

-	Layers:
	-	`sha256:cef5adb75bd4691035af00bb58c196f619708318815fbacb1530a9b61bd70928`  
		Last Modified: Wed, 16 Oct 2024 01:37:07 GMT  
		Size: 5.8 MB (5845864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36ba4e72ad602c58ca8b885b6546cd8f3a928aab197feaec86dbda22889c4a`  
		Last Modified: Wed, 16 Oct 2024 01:37:06 GMT  
		Size: 20.7 KB (20736 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:aecd06ae59ffa1ce84272c31aa0cba385bc20ee40694b5fd94563f3107e96700
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:11f8cce84ec751a7d20fca0cd8869e22df8bb3e3d32ef535ba07939ec4fa8e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297982036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a6616c54689264a1d2e6135363fd2c98ac4c79e8543f4ad800a1d91dd219c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8d28d5756fd38a4b3d4cb29bed83b190b30336d4a8d0edae89a92a6bc18785`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 130.5 MB (130471633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3379440813b187578ecb4f2b3737839a7f983df12d22ee11efb811957730712a`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b45dc9a5fd807a802206d70e1cfa2d07c77c4a92a03af0d01965369b2f804a`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 128.4 MB (128398662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:85cfc55c3194b2e4e996a512c90ff90261b4ce5632e45a4d6d92bcc159003d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5596767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a997650cfd9cbf57da31612b46cc0a1a74a7153caa7a2afc6a094c7121208`

```dockerfile
```

-	Layers:
	-	`sha256:1714d8e4ee1853bd2b8e39fa1646979557f9433de6a80f0eab004ccf6f7893a2`  
		Last Modified: Thu, 03 Oct 2024 16:58:23 GMT  
		Size: 5.6 MB (5574999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c64bd46995faa9273d359b075335da3d023bf27c57ccba375ce282e0009a9d`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 21.8 KB (21768 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:80904012ea7f7ecf62b6852b1133cb8fcc78b93cc7d816ce12b8e63b0dce69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295756870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7beb8d486e41da40ece889f83e6f4b75bc6f2630c00297fe3eeee09ba9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e86b65debcab04675289daf0519879958a8b08fdd7f6d3c75e2812f6ab8b5`  
		Last Modified: Wed, 16 Oct 2024 01:35:55 GMT  
		Size: 128.4 MB (128429899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bdc718fa20e132153311b5cb54d7249eeb3bc7c737fcc6111c9ab804b96c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f82734a381690c7ea06cda6e16842718abb9b16cb0d6c26ac7b48d1e51afbb`

```dockerfile
```

-	Layers:
	-	`sha256:3cef2b4c281264da4ef550401c4d2e03c35de852d05e71cfcd46a32d9fda5a27`  
		Last Modified: Wed, 16 Oct 2024 01:35:53 GMT  
		Size: 5.6 MB (5555861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81269aefe8951f03d6e5eac745ace7a473319c8003405930f95a5e9ce8dbf56f`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24-bullseye`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24-community`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24-community-bullseye`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24-community-ubi9`

```console
$ docker pull neo4j@sha256:aecd06ae59ffa1ce84272c31aa0cba385bc20ee40694b5fd94563f3107e96700
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:11f8cce84ec751a7d20fca0cd8869e22df8bb3e3d32ef535ba07939ec4fa8e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297982036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a6616c54689264a1d2e6135363fd2c98ac4c79e8543f4ad800a1d91dd219c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8d28d5756fd38a4b3d4cb29bed83b190b30336d4a8d0edae89a92a6bc18785`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 130.5 MB (130471633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3379440813b187578ecb4f2b3737839a7f983df12d22ee11efb811957730712a`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b45dc9a5fd807a802206d70e1cfa2d07c77c4a92a03af0d01965369b2f804a`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 128.4 MB (128398662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:85cfc55c3194b2e4e996a512c90ff90261b4ce5632e45a4d6d92bcc159003d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5596767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a997650cfd9cbf57da31612b46cc0a1a74a7153caa7a2afc6a094c7121208`

```dockerfile
```

-	Layers:
	-	`sha256:1714d8e4ee1853bd2b8e39fa1646979557f9433de6a80f0eab004ccf6f7893a2`  
		Last Modified: Thu, 03 Oct 2024 16:58:23 GMT  
		Size: 5.6 MB (5574999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c64bd46995faa9273d359b075335da3d023bf27c57ccba375ce282e0009a9d`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 21.8 KB (21768 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:80904012ea7f7ecf62b6852b1133cb8fcc78b93cc7d816ce12b8e63b0dce69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295756870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7beb8d486e41da40ece889f83e6f4b75bc6f2630c00297fe3eeee09ba9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e86b65debcab04675289daf0519879958a8b08fdd7f6d3c75e2812f6ab8b5`  
		Last Modified: Wed, 16 Oct 2024 01:35:55 GMT  
		Size: 128.4 MB (128429899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bdc718fa20e132153311b5cb54d7249eeb3bc7c737fcc6111c9ab804b96c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f82734a381690c7ea06cda6e16842718abb9b16cb0d6c26ac7b48d1e51afbb`

```dockerfile
```

-	Layers:
	-	`sha256:3cef2b4c281264da4ef550401c4d2e03c35de852d05e71cfcd46a32d9fda5a27`  
		Last Modified: Wed, 16 Oct 2024 01:35:53 GMT  
		Size: 5.6 MB (5555861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81269aefe8951f03d6e5eac745ace7a473319c8003405930f95a5e9ce8dbf56f`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24-enterprise`

```console
$ docker pull neo4j@sha256:0666f8ae5c7d34abf7b20b6e90c4a207d0d362bf6305e1a8dfdff54bcc3c4ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:590c27d5bba2d730565a557a7814fa882a9f15e04c1764cb201eabab9e604eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594431321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72a2667dc06e9e63841b1c356d91f347e325e651cc781bcdd02fc41feed89`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4795283092d21e11e6420af407ae339d038ee0f6e57eff13590d16716114c`  
		Last Modified: Sat, 12 Oct 2024 00:55:41 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e53848ab5f1a212ed1451e202eb7325a4265c9b6aaac6d17b7199b032740`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b411f01df6bc07ae62e8f24d3ca78ff67f63d59140b4c506941d4ee04f045b`  
		Last Modified: Sat, 12 Oct 2024 00:55:44 GMT  
		Size: 417.8 MB (417822283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f183703ddeef3cd31de960d02e0d63ebfb6a09c288771ac5ff7d3dcaa4303d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfe855c2d8e2c85eb0f650e6be7e05309957de9c404fac9c7935fc96237ef2`

```dockerfile
```

-	Layers:
	-	`sha256:c7841d8712194410176ae5e538da763bce05265594ba1741489a587ae6b2841a`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 3.5 MB (3467938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbdf2a9fb713de81bdfd1ceb95b57146364555e4dbda32e86b05fb613ca526f`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0a9a826c3f3b5bbdc0f188d1862f72ad03344b625e61ce627a4a3c8e8f419fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591834754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96b88717f157516a6a72a8f1c99e2d053265b93709f800b6f89b6d6dc6c0981`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b8b2c0c6cbf5bd6f5f098210e2abbdbc8ec35b22022f7c15a1ca516db6497`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5362fc052deffc3962231d660dd131a36f151e07c3f2796d2d2045762cd91f2`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22290c1bb6fe3fb6d51d60ed418901680becc046f0effeded324de024cd5bdb`  
		Last Modified: Sat, 12 Oct 2024 01:56:34 GMT  
		Size: 417.8 MB (417786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2450a25f361d6b8e8413145e18c89ed22c0a149a0fe9b5cfca51edfb2ad3830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2f46402ccc6f78e666f88b8fcf0256ee38942feaa3761d0b1835564992ef54`

```dockerfile
```

-	Layers:
	-	`sha256:855a223e9a1bfe6e68ef987d624a20d21838a7430894da4715eb38ff6b64703b`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.5 MB (3467630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700782de77acf9194d6a3c16de88d92c3ba35c50fdf2ffd2fef5fb5757057a45`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 21.2 KB (21237 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:0666f8ae5c7d34abf7b20b6e90c4a207d0d362bf6305e1a8dfdff54bcc3c4ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:590c27d5bba2d730565a557a7814fa882a9f15e04c1764cb201eabab9e604eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594431321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72a2667dc06e9e63841b1c356d91f347e325e651cc781bcdd02fc41feed89`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4795283092d21e11e6420af407ae339d038ee0f6e57eff13590d16716114c`  
		Last Modified: Sat, 12 Oct 2024 00:55:41 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e53848ab5f1a212ed1451e202eb7325a4265c9b6aaac6d17b7199b032740`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b411f01df6bc07ae62e8f24d3ca78ff67f63d59140b4c506941d4ee04f045b`  
		Last Modified: Sat, 12 Oct 2024 00:55:44 GMT  
		Size: 417.8 MB (417822283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f183703ddeef3cd31de960d02e0d63ebfb6a09c288771ac5ff7d3dcaa4303d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfe855c2d8e2c85eb0f650e6be7e05309957de9c404fac9c7935fc96237ef2`

```dockerfile
```

-	Layers:
	-	`sha256:c7841d8712194410176ae5e538da763bce05265594ba1741489a587ae6b2841a`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 3.5 MB (3467938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbdf2a9fb713de81bdfd1ceb95b57146364555e4dbda32e86b05fb613ca526f`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0a9a826c3f3b5bbdc0f188d1862f72ad03344b625e61ce627a4a3c8e8f419fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591834754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96b88717f157516a6a72a8f1c99e2d053265b93709f800b6f89b6d6dc6c0981`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b8b2c0c6cbf5bd6f5f098210e2abbdbc8ec35b22022f7c15a1ca516db6497`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5362fc052deffc3962231d660dd131a36f151e07c3f2796d2d2045762cd91f2`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22290c1bb6fe3fb6d51d60ed418901680becc046f0effeded324de024cd5bdb`  
		Last Modified: Sat, 12 Oct 2024 01:56:34 GMT  
		Size: 417.8 MB (417786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2450a25f361d6b8e8413145e18c89ed22c0a149a0fe9b5cfca51edfb2ad3830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2f46402ccc6f78e666f88b8fcf0256ee38942feaa3761d0b1835564992ef54`

```dockerfile
```

-	Layers:
	-	`sha256:855a223e9a1bfe6e68ef987d624a20d21838a7430894da4715eb38ff6b64703b`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.5 MB (3467630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700782de77acf9194d6a3c16de88d92c3ba35c50fdf2ffd2fef5fb5757057a45`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 21.2 KB (21237 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:06186ebe260bba187b9232406b0f6512fa2bf6492c43bb4211c01ff63d0fc414
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c5165682e4c3184b98ffa78364e182f6e140d7ba80bc13d1471c33a42936ca4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584476713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75814d862d65790d31cf7452aad9bb4582b322aea1cf53a4c208da73f0f427d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a2667db7626e9689afefaaa859d8c99203a4c5848ab291f86aa7e6ee5652a9`  
		Last Modified: Thu, 03 Oct 2024 16:58:36 GMT  
		Size: 130.5 MB (130471618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd8e20163536ab988cee7f3eb02797ed6dc49269a1aad93bab95dee73b069f4`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 10.0 KB (10008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df727bcd4b740fb7d4ae1f82b2b12e9eebe3432a6c50f5cecb51a636880ded51`  
		Last Modified: Thu, 03 Oct 2024 16:58:40 GMT  
		Size: 414.9 MB (414893355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1b3bb6c78d7b647b520c7dc40464faa4eb456aa0e0feba51887001060fb0180c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5885640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5e321376f7e52ca4cc75752515fb52064e18a51defe09b023c9d2bce65899`

```dockerfile
```

-	Layers:
	-	`sha256:ffa8a0578ce6b7b6b2335553e37d033634b25be3db137ad8f2933613a3dd8849`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 5.9 MB (5865050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0441d0f852989cb183733f03b4969085b83c5b591b902e1bf186b98884e674b`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 20.6 KB (20590 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:304f60f068da68eafe8da73e574cb59db92c25571092ab2bac6c5e1f93b44ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582250395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48eeb41d00ac2c2187f0755fe26096557c659ed4793515c7d6ba628b296dc2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7ce97bd9a4348af14df442f00b3dc5085b5983d6f03da643744838c7a1bc8ba7 NEO4J_TARBALL=neo4j-enterprise-5.24.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf5c8d1888bff8b7e1efdfa99f2e3c6cc5d44ed7273695b14636614f5df1146`  
		Last Modified: Wed, 16 Oct 2024 01:37:15 GMT  
		Size: 414.9 MB (414923424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5fc0196480e8c3bcff8ee15cfd7f0c99c05bc0330b81021887e19eff6a994bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5866600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18754f5534ac8404dcd3b51edfe12611f21787d70f53e57b4e16ce866c338683`

```dockerfile
```

-	Layers:
	-	`sha256:cef5adb75bd4691035af00bb58c196f619708318815fbacb1530a9b61bd70928`  
		Last Modified: Wed, 16 Oct 2024 01:37:07 GMT  
		Size: 5.8 MB (5845864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36ba4e72ad602c58ca8b885b6546cd8f3a928aab197feaec86dbda22889c4a`  
		Last Modified: Wed, 16 Oct 2024 01:37:06 GMT  
		Size: 20.7 KB (20736 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24-ubi9`

```console
$ docker pull neo4j@sha256:aecd06ae59ffa1ce84272c31aa0cba385bc20ee40694b5fd94563f3107e96700
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:11f8cce84ec751a7d20fca0cd8869e22df8bb3e3d32ef535ba07939ec4fa8e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297982036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a6616c54689264a1d2e6135363fd2c98ac4c79e8543f4ad800a1d91dd219c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8d28d5756fd38a4b3d4cb29bed83b190b30336d4a8d0edae89a92a6bc18785`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 130.5 MB (130471633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3379440813b187578ecb4f2b3737839a7f983df12d22ee11efb811957730712a`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b45dc9a5fd807a802206d70e1cfa2d07c77c4a92a03af0d01965369b2f804a`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 128.4 MB (128398662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:85cfc55c3194b2e4e996a512c90ff90261b4ce5632e45a4d6d92bcc159003d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5596767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a997650cfd9cbf57da31612b46cc0a1a74a7153caa7a2afc6a094c7121208`

```dockerfile
```

-	Layers:
	-	`sha256:1714d8e4ee1853bd2b8e39fa1646979557f9433de6a80f0eab004ccf6f7893a2`  
		Last Modified: Thu, 03 Oct 2024 16:58:23 GMT  
		Size: 5.6 MB (5574999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c64bd46995faa9273d359b075335da3d023bf27c57ccba375ce282e0009a9d`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 21.8 KB (21768 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.24-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:80904012ea7f7ecf62b6852b1133cb8fcc78b93cc7d816ce12b8e63b0dce69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295756870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7beb8d486e41da40ece889f83e6f4b75bc6f2630c00297fe3eeee09ba9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e86b65debcab04675289daf0519879958a8b08fdd7f6d3c75e2812f6ab8b5`  
		Last Modified: Wed, 16 Oct 2024 01:35:55 GMT  
		Size: 128.4 MB (128429899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bdc718fa20e132153311b5cb54d7249eeb3bc7c737fcc6111c9ab804b96c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f82734a381690c7ea06cda6e16842718abb9b16cb0d6c26ac7b48d1e51afbb`

```dockerfile
```

-	Layers:
	-	`sha256:3cef2b4c281264da4ef550401c4d2e03c35de852d05e71cfcd46a32d9fda5a27`  
		Last Modified: Wed, 16 Oct 2024 01:35:53 GMT  
		Size: 5.6 MB (5555861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81269aefe8951f03d6e5eac745ace7a473319c8003405930f95a5e9ce8dbf56f`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24.2`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.24.2-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.24.2-community`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.24.2-community-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.24.2-community-ubi9`

```console
$ docker pull neo4j@sha256:a91135e5442f27062c034b54020d652b32e3fbd8bc283b834afe881d6a2ad8d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24.2-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:80904012ea7f7ecf62b6852b1133cb8fcc78b93cc7d816ce12b8e63b0dce69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295756870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7beb8d486e41da40ece889f83e6f4b75bc6f2630c00297fe3eeee09ba9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e86b65debcab04675289daf0519879958a8b08fdd7f6d3c75e2812f6ab8b5`  
		Last Modified: Wed, 16 Oct 2024 01:35:55 GMT  
		Size: 128.4 MB (128429899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24.2-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bdc718fa20e132153311b5cb54d7249eeb3bc7c737fcc6111c9ab804b96c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f82734a381690c7ea06cda6e16842718abb9b16cb0d6c26ac7b48d1e51afbb`

```dockerfile
```

-	Layers:
	-	`sha256:3cef2b4c281264da4ef550401c4d2e03c35de852d05e71cfcd46a32d9fda5a27`  
		Last Modified: Wed, 16 Oct 2024 01:35:53 GMT  
		Size: 5.6 MB (5555861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81269aefe8951f03d6e5eac745ace7a473319c8003405930f95a5e9ce8dbf56f`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24.2-enterprise`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.24.2-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.24.2-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:dc7f9bc716f82d59a013ee1a74ee635b63b989b14227800692e0e89bf3ce927a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24.2-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:304f60f068da68eafe8da73e574cb59db92c25571092ab2bac6c5e1f93b44ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582250395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48eeb41d00ac2c2187f0755fe26096557c659ed4793515c7d6ba628b296dc2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7ce97bd9a4348af14df442f00b3dc5085b5983d6f03da643744838c7a1bc8ba7 NEO4J_TARBALL=neo4j-enterprise-5.24.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf5c8d1888bff8b7e1efdfa99f2e3c6cc5d44ed7273695b14636614f5df1146`  
		Last Modified: Wed, 16 Oct 2024 01:37:15 GMT  
		Size: 414.9 MB (414923424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24.2-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5fc0196480e8c3bcff8ee15cfd7f0c99c05bc0330b81021887e19eff6a994bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5866600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18754f5534ac8404dcd3b51edfe12611f21787d70f53e57b4e16ce866c338683`

```dockerfile
```

-	Layers:
	-	`sha256:cef5adb75bd4691035af00bb58c196f619708318815fbacb1530a9b61bd70928`  
		Last Modified: Wed, 16 Oct 2024 01:37:07 GMT  
		Size: 5.8 MB (5845864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36ba4e72ad602c58ca8b885b6546cd8f3a928aab197feaec86dbda22889c4a`  
		Last Modified: Wed, 16 Oct 2024 01:37:06 GMT  
		Size: 20.7 KB (20736 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24.2-ubi9`

```console
$ docker pull neo4j@sha256:a91135e5442f27062c034b54020d652b32e3fbd8bc283b834afe881d6a2ad8d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.24.2-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:80904012ea7f7ecf62b6852b1133cb8fcc78b93cc7d816ce12b8e63b0dce69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295756870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7beb8d486e41da40ece889f83e6f4b75bc6f2630c00297fe3eeee09ba9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e86b65debcab04675289daf0519879958a8b08fdd7f6d3c75e2812f6ab8b5`  
		Last Modified: Wed, 16 Oct 2024 01:35:55 GMT  
		Size: 128.4 MB (128429899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.24.2-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bdc718fa20e132153311b5cb54d7249eeb3bc7c737fcc6111c9ab804b96c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f82734a381690c7ea06cda6e16842718abb9b16cb0d6c26ac7b48d1e51afbb`

```dockerfile
```

-	Layers:
	-	`sha256:3cef2b4c281264da4ef550401c4d2e03c35de852d05e71cfcd46a32d9fda5a27`  
		Last Modified: Wed, 16 Oct 2024 01:35:53 GMT  
		Size: 5.6 MB (5555861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81269aefe8951f03d6e5eac745ace7a473319c8003405930f95a5e9ce8dbf56f`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:aecd06ae59ffa1ce84272c31aa0cba385bc20ee40694b5fd94563f3107e96700
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:11f8cce84ec751a7d20fca0cd8869e22df8bb3e3d32ef535ba07939ec4fa8e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297982036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a6616c54689264a1d2e6135363fd2c98ac4c79e8543f4ad800a1d91dd219c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8d28d5756fd38a4b3d4cb29bed83b190b30336d4a8d0edae89a92a6bc18785`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 130.5 MB (130471633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3379440813b187578ecb4f2b3737839a7f983df12d22ee11efb811957730712a`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b45dc9a5fd807a802206d70e1cfa2d07c77c4a92a03af0d01965369b2f804a`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 128.4 MB (128398662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:85cfc55c3194b2e4e996a512c90ff90261b4ce5632e45a4d6d92bcc159003d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5596767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a997650cfd9cbf57da31612b46cc0a1a74a7153caa7a2afc6a094c7121208`

```dockerfile
```

-	Layers:
	-	`sha256:1714d8e4ee1853bd2b8e39fa1646979557f9433de6a80f0eab004ccf6f7893a2`  
		Last Modified: Thu, 03 Oct 2024 16:58:23 GMT  
		Size: 5.6 MB (5574999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c64bd46995faa9273d359b075335da3d023bf27c57ccba375ce282e0009a9d`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 21.8 KB (21768 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:80904012ea7f7ecf62b6852b1133cb8fcc78b93cc7d816ce12b8e63b0dce69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295756870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7beb8d486e41da40ece889f83e6f4b75bc6f2630c00297fe3eeee09ba9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e86b65debcab04675289daf0519879958a8b08fdd7f6d3c75e2812f6ab8b5`  
		Last Modified: Wed, 16 Oct 2024 01:35:55 GMT  
		Size: 128.4 MB (128429899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bdc718fa20e132153311b5cb54d7249eeb3bc7c737fcc6111c9ab804b96c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f82734a381690c7ea06cda6e16842718abb9b16cb0d6c26ac7b48d1e51afbb`

```dockerfile
```

-	Layers:
	-	`sha256:3cef2b4c281264da4ef550401c4d2e03c35de852d05e71cfcd46a32d9fda5a27`  
		Last Modified: Wed, 16 Oct 2024 01:35:53 GMT  
		Size: 5.6 MB (5555861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81269aefe8951f03d6e5eac745ace7a473319c8003405930f95a5e9ce8dbf56f`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:0666f8ae5c7d34abf7b20b6e90c4a207d0d362bf6305e1a8dfdff54bcc3c4ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:590c27d5bba2d730565a557a7814fa882a9f15e04c1764cb201eabab9e604eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594431321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72a2667dc06e9e63841b1c356d91f347e325e651cc781bcdd02fc41feed89`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4795283092d21e11e6420af407ae339d038ee0f6e57eff13590d16716114c`  
		Last Modified: Sat, 12 Oct 2024 00:55:41 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e53848ab5f1a212ed1451e202eb7325a4265c9b6aaac6d17b7199b032740`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b411f01df6bc07ae62e8f24d3ca78ff67f63d59140b4c506941d4ee04f045b`  
		Last Modified: Sat, 12 Oct 2024 00:55:44 GMT  
		Size: 417.8 MB (417822283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f183703ddeef3cd31de960d02e0d63ebfb6a09c288771ac5ff7d3dcaa4303d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfe855c2d8e2c85eb0f650e6be7e05309957de9c404fac9c7935fc96237ef2`

```dockerfile
```

-	Layers:
	-	`sha256:c7841d8712194410176ae5e538da763bce05265594ba1741489a587ae6b2841a`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 3.5 MB (3467938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbdf2a9fb713de81bdfd1ceb95b57146364555e4dbda32e86b05fb613ca526f`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0a9a826c3f3b5bbdc0f188d1862f72ad03344b625e61ce627a4a3c8e8f419fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591834754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96b88717f157516a6a72a8f1c99e2d053265b93709f800b6f89b6d6dc6c0981`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b8b2c0c6cbf5bd6f5f098210e2abbdbc8ec35b22022f7c15a1ca516db6497`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5362fc052deffc3962231d660dd131a36f151e07c3f2796d2d2045762cd91f2`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22290c1bb6fe3fb6d51d60ed418901680becc046f0effeded324de024cd5bdb`  
		Last Modified: Sat, 12 Oct 2024 01:56:34 GMT  
		Size: 417.8 MB (417786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2450a25f361d6b8e8413145e18c89ed22c0a149a0fe9b5cfca51edfb2ad3830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2f46402ccc6f78e666f88b8fcf0256ee38942feaa3761d0b1835564992ef54`

```dockerfile
```

-	Layers:
	-	`sha256:855a223e9a1bfe6e68ef987d624a20d21838a7430894da4715eb38ff6b64703b`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.5 MB (3467630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700782de77acf9194d6a3c16de88d92c3ba35c50fdf2ffd2fef5fb5757057a45`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 21.2 KB (21237 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:0666f8ae5c7d34abf7b20b6e90c4a207d0d362bf6305e1a8dfdff54bcc3c4ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:590c27d5bba2d730565a557a7814fa882a9f15e04c1764cb201eabab9e604eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594431321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72a2667dc06e9e63841b1c356d91f347e325e651cc781bcdd02fc41feed89`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4795283092d21e11e6420af407ae339d038ee0f6e57eff13590d16716114c`  
		Last Modified: Sat, 12 Oct 2024 00:55:41 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e53848ab5f1a212ed1451e202eb7325a4265c9b6aaac6d17b7199b032740`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b411f01df6bc07ae62e8f24d3ca78ff67f63d59140b4c506941d4ee04f045b`  
		Last Modified: Sat, 12 Oct 2024 00:55:44 GMT  
		Size: 417.8 MB (417822283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f183703ddeef3cd31de960d02e0d63ebfb6a09c288771ac5ff7d3dcaa4303d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfe855c2d8e2c85eb0f650e6be7e05309957de9c404fac9c7935fc96237ef2`

```dockerfile
```

-	Layers:
	-	`sha256:c7841d8712194410176ae5e538da763bce05265594ba1741489a587ae6b2841a`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 3.5 MB (3467938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbdf2a9fb713de81bdfd1ceb95b57146364555e4dbda32e86b05fb613ca526f`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0a9a826c3f3b5bbdc0f188d1862f72ad03344b625e61ce627a4a3c8e8f419fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591834754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96b88717f157516a6a72a8f1c99e2d053265b93709f800b6f89b6d6dc6c0981`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b8b2c0c6cbf5bd6f5f098210e2abbdbc8ec35b22022f7c15a1ca516db6497`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5362fc052deffc3962231d660dd131a36f151e07c3f2796d2d2045762cd91f2`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22290c1bb6fe3fb6d51d60ed418901680becc046f0effeded324de024cd5bdb`  
		Last Modified: Sat, 12 Oct 2024 01:56:34 GMT  
		Size: 417.8 MB (417786173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2450a25f361d6b8e8413145e18c89ed22c0a149a0fe9b5cfca51edfb2ad3830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2f46402ccc6f78e666f88b8fcf0256ee38942feaa3761d0b1835564992ef54`

```dockerfile
```

-	Layers:
	-	`sha256:855a223e9a1bfe6e68ef987d624a20d21838a7430894da4715eb38ff6b64703b`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 3.5 MB (3467630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700782de77acf9194d6a3c16de88d92c3ba35c50fdf2ffd2fef5fb5757057a45`  
		Last Modified: Sat, 12 Oct 2024 01:56:26 GMT  
		Size: 21.2 KB (21237 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:06186ebe260bba187b9232406b0f6512fa2bf6492c43bb4211c01ff63d0fc414
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c5165682e4c3184b98ffa78364e182f6e140d7ba80bc13d1471c33a42936ca4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584476713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75814d862d65790d31cf7452aad9bb4582b322aea1cf53a4c208da73f0f427d3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a2667db7626e9689afefaaa859d8c99203a4c5848ab291f86aa7e6ee5652a9`  
		Last Modified: Thu, 03 Oct 2024 16:58:36 GMT  
		Size: 130.5 MB (130471618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd8e20163536ab988cee7f3eb02797ed6dc49269a1aad93bab95dee73b069f4`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 10.0 KB (10008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df727bcd4b740fb7d4ae1f82b2b12e9eebe3432a6c50f5cecb51a636880ded51`  
		Last Modified: Thu, 03 Oct 2024 16:58:40 GMT  
		Size: 414.9 MB (414893355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1b3bb6c78d7b647b520c7dc40464faa4eb456aa0e0feba51887001060fb0180c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5885640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5e321376f7e52ca4cc75752515fb52064e18a51defe09b023c9d2bce65899`

```dockerfile
```

-	Layers:
	-	`sha256:ffa8a0578ce6b7b6b2335553e37d033634b25be3db137ad8f2933613a3dd8849`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 5.9 MB (5865050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0441d0f852989cb183733f03b4969085b83c5b591b902e1bf186b98884e674b`  
		Last Modified: Thu, 03 Oct 2024 16:58:34 GMT  
		Size: 20.6 KB (20590 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:304f60f068da68eafe8da73e574cb59db92c25571092ab2bac6c5e1f93b44ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582250395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48eeb41d00ac2c2187f0755fe26096557c659ed4793515c7d6ba628b296dc2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7ce97bd9a4348af14df442f00b3dc5085b5983d6f03da643744838c7a1bc8ba7 NEO4J_TARBALL=neo4j-enterprise-5.24.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf5c8d1888bff8b7e1efdfa99f2e3c6cc5d44ed7273695b14636614f5df1146`  
		Last Modified: Wed, 16 Oct 2024 01:37:15 GMT  
		Size: 414.9 MB (414923424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5fc0196480e8c3bcff8ee15cfd7f0c99c05bc0330b81021887e19eff6a994bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5866600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18754f5534ac8404dcd3b51edfe12611f21787d70f53e57b4e16ce866c338683`

```dockerfile
```

-	Layers:
	-	`sha256:cef5adb75bd4691035af00bb58c196f619708318815fbacb1530a9b61bd70928`  
		Last Modified: Wed, 16 Oct 2024 01:37:07 GMT  
		Size: 5.8 MB (5845864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36ba4e72ad602c58ca8b885b6546cd8f3a928aab197feaec86dbda22889c4a`  
		Last Modified: Wed, 16 Oct 2024 01:37:06 GMT  
		Size: 20.7 KB (20736 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:8c0c8528b7876053ce49d8e0c27958c083a0b0d8f5ae2f38390a4df95b96af9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cb1553d2fe22a1bfbfc4550463ea411a6fbe13d8e6ae8079b7eca25a07a8720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305345352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d447c32d6f58b25e4718ddd0b95815a91590dfc4a89451371498ec9b1f19fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa8b0ff27bdece2d729f5de31d80af7cd7521875c11d7c8238257fc0d96a1c`  
		Last Modified: Sat, 12 Oct 2024 01:16:40 GMT  
		Size: 144.0 MB (143959510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0752fed69cee5aa2d32305fc9e8e865a049479b781264c2d6029847d3a3543d1`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed158f509b44e997be56474dd3d4fe18a8d106c77d3cbd07bb95f915105f057`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9cc6dcd5ef5b2f955161bb435106bad84cc69f570af8712c8c6f8971ba7ba`  
		Last Modified: Sat, 12 Oct 2024 01:55:10 GMT  
		Size: 131.3 MB (131296771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:c025b0c367a69abd5ff47e984222f0c5b7ee1876d6b503fbbf346695f67b0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0833e44da67dcc76da97e0085dcfe3c7b87942dc91ad004cb654e9e006d0b7`

```dockerfile
```

-	Layers:
	-	`sha256:88ad54251ae690fd9fc18be6098c1b853e400ad1f978da9d6b01ca2c12f26b46`  
		Last Modified: Sat, 12 Oct 2024 01:55:08 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612f1d464a37235aada14a72284d41914598ec9ae95b88377cb04c4f9eb8979a`  
		Last Modified: Sat, 12 Oct 2024 01:55:07 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:aecd06ae59ffa1ce84272c31aa0cba385bc20ee40694b5fd94563f3107e96700
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:11f8cce84ec751a7d20fca0cd8869e22df8bb3e3d32ef535ba07939ec4fa8e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297982036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a6616c54689264a1d2e6135363fd2c98ac4c79e8543f4ad800a1d91dd219c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:41 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Wed, 18 Sep 2024 21:29:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:42 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:42 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:42 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:43 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:43 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 03 Oct 2024 12:51:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8d28d5756fd38a4b3d4cb29bed83b190b30336d4a8d0edae89a92a6bc18785`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 130.5 MB (130471633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3379440813b187578ecb4f2b3737839a7f983df12d22ee11efb811957730712a`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b45dc9a5fd807a802206d70e1cfa2d07c77c4a92a03af0d01965369b2f804a`  
		Last Modified: Thu, 03 Oct 2024 16:58:24 GMT  
		Size: 128.4 MB (128398662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:85cfc55c3194b2e4e996a512c90ff90261b4ce5632e45a4d6d92bcc159003d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5596767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a997650cfd9cbf57da31612b46cc0a1a74a7153caa7a2afc6a094c7121208`

```dockerfile
```

-	Layers:
	-	`sha256:1714d8e4ee1853bd2b8e39fa1646979557f9433de6a80f0eab004ccf6f7893a2`  
		Last Modified: Thu, 03 Oct 2024 16:58:23 GMT  
		Size: 5.6 MB (5574999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c64bd46995faa9273d359b075335da3d023bf27c57ccba375ce282e0009a9d`  
		Last Modified: Thu, 03 Oct 2024 16:58:22 GMT  
		Size: 21.8 KB (21768 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:80904012ea7f7ecf62b6852b1133cb8fcc78b93cc7d816ce12b8e63b0dce69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295756870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7beb8d486e41da40ece889f83e6f4b75bc6f2630c00297fe3eeee09ba9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Sep 2024 21:29:42 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Wed, 18 Sep 2024 21:29:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:29:43 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:29:44 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:29:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Sep 2024 21:29:44 GMT
ENV container oci
# Wed, 18 Sep 2024 21:29:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:29:44 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:29:45 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Wed, 18 Sep 2024 21:29:45 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Wed, 18 Sep 2024 21:29:45 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Wed, 18 Sep 2024 21:29:46 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:29:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:29:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 15 Oct 2024 14:23:38 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eedb0866fa9bc4bb72c8701b114a8fab0df211212ed7cab717305087bbdb3fe`  
		Last Modified: Wed, 16 Oct 2024 01:35:56 GMT  
		Size: 130.0 MB (129981516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8278895945dffae579db5c6f7be854ae24b0beeba856e5af10baa221b57b347`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656e86b65debcab04675289daf0519879958a8b08fdd7f6d3c75e2812f6ab8b5`  
		Last Modified: Wed, 16 Oct 2024 01:35:55 GMT  
		Size: 128.4 MB (128429899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bdc718fa20e132153311b5cb54d7249eeb3bc7c737fcc6111c9ab804b96c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f82734a381690c7ea06cda6e16842718abb9b16cb0d6c26ac7b48d1e51afbb`

```dockerfile
```

-	Layers:
	-	`sha256:3cef2b4c281264da4ef550401c4d2e03c35de852d05e71cfcd46a32d9fda5a27`  
		Last Modified: Wed, 16 Oct 2024 01:35:53 GMT  
		Size: 5.6 MB (5555861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81269aefe8951f03d6e5eac745ace7a473319c8003405930f95a5e9ce8dbf56f`  
		Last Modified: Wed, 16 Oct 2024 01:35:52 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json
