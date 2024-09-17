<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.37`](#neo4j4437)
-	[`neo4j:4.4.37-community`](#neo4j4437-community)
-	[`neo4j:4.4.37-enterprise`](#neo4j4437-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi9`](#neo4j5-community-ubi9)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi9`](#neo4j5-enterprise-ubi9)
-	[`neo4j:5-ubi9`](#neo4j5-ubi9)
-	[`neo4j:5.23`](#neo4j523)
-	[`neo4j:5.23-bullseye`](#neo4j523-bullseye)
-	[`neo4j:5.23-community`](#neo4j523-community)
-	[`neo4j:5.23-community-bullseye`](#neo4j523-community-bullseye)
-	[`neo4j:5.23-community-ubi9`](#neo4j523-community-ubi9)
-	[`neo4j:5.23-enterprise`](#neo4j523-enterprise)
-	[`neo4j:5.23-enterprise-bullseye`](#neo4j523-enterprise-bullseye)
-	[`neo4j:5.23-enterprise-ubi9`](#neo4j523-enterprise-ubi9)
-	[`neo4j:5.23-ubi9`](#neo4j523-ubi9)
-	[`neo4j:5.23.0`](#neo4j5230)
-	[`neo4j:5.23.0-bullseye`](#neo4j5230-bullseye)
-	[`neo4j:5.23.0-community`](#neo4j5230-community)
-	[`neo4j:5.23.0-community-bullseye`](#neo4j5230-community-bullseye)
-	[`neo4j:5.23.0-community-ubi9`](#neo4j5230-community-ubi9)
-	[`neo4j:5.23.0-enterprise`](#neo4j5230-enterprise)
-	[`neo4j:5.23.0-enterprise-bullseye`](#neo4j5230-enterprise-bullseye)
-	[`neo4j:5.23.0-enterprise-ubi9`](#neo4j5230-enterprise-ubi9)
-	[`neo4j:5.23.0-ubi9`](#neo4j5230-ubi9)
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
$ docker pull neo4j@sha256:3fd0cb66f1de75d4451df1e05076e0a7098668b9acaa7cbfc988b58352001de9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:6865ada3f9be9adecdb91b3e1de7417f77715f513e659280b71f2c1846cad7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303073182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f08890e624437ca9667e894b93d4d0b18679e90e15c4a987220ba18c2cf1ead`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335e27b066f2c1c0bbeed39461a4a4fbf62a055865b375718b8f3b7829c7847`  
		Last Modified: Tue, 17 Sep 2024 01:57:46 GMT  
		Size: 145.6 MB (145550136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699c1af577d1d31fea174323154f98d80ebf0799a1653d1e16aa757dac2c0c5`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27537114c753be34bde0119da8822af92999c188c8179fae5d7818485ab1cc9`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cea4cf567c848a35ef033f3c580f5a9bb292d07e467b8b3fec2deb5b9ded5e`  
		Last Modified: Tue, 17 Sep 2024 01:57:46 GMT  
		Size: 126.1 MB (126080975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a45e091d1cf5d5b390d9186fbf47928cb8614e1a5e4c95c4c1d042010cdfc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1914764b74990c81519ecd791f43a90562a24488c06bd003f3989dbab719b95b`

```dockerfile
```

-	Layers:
	-	`sha256:9f7fef84eee0581296c386829208bb5a50f32d46fc94de3a2da8731bb14fe636`  
		Last Modified: Tue, 17 Sep 2024 01:57:45 GMT  
		Size: 3.0 MB (2993152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f576ad7926e77a49b4c68a367bc30414ad45aee426f6e47e6627bf2dbccb7fe6`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 19.6 KB (19590 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5114d2ce8cf864df0d46b61a83efc9091a8a9f541fd5a0552203f9f7a6b3bd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298486868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee3208ccef8bed14f5f24d2cfe75534065dc74ea62e33279b74c18454c46b57`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c14ea5bd28a65eb584dbc13e080a28deed5b2dfc84ae2658426304af8f58515`  
		Last Modified: Thu, 05 Sep 2024 07:57:40 GMT  
		Size: 142.4 MB (142354887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2c05e06974abd1044f3b0a63655c85405a56f40cfefdcee71e98502faab76`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20ff0775c7a1e3a4695b5d446055e4ab7f86102da49dc9c81c296a3bcd57c08`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bb011871fdbda36fb83ea88a689aa087392ca243e4d01d7f7e8a48716aa5c`  
		Last Modified: Thu, 05 Sep 2024 22:22:28 GMT  
		Size: 126.0 MB (126044198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:bc9fb8fd6a2fc43d5ce841f8fc3800281c9336e2811bddf1013b15c7334b8788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d3d6d3248fcc7591237b1ce354f945e9c33e5e84bc811085eae0701df49b84`

```dockerfile
```

-	Layers:
	-	`sha256:c040a018d8d37b7b505f65b239525cd2b5220b784eddd8370ee92f94351a0195`  
		Last Modified: Thu, 05 Sep 2024 22:22:25 GMT  
		Size: 3.0 MB (2993988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8010ffea3ea7365cadcf5b422e457388d09feb73efdaa0734d0a1f097320ce93`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 20.1 KB (20143 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:3fd0cb66f1de75d4451df1e05076e0a7098668b9acaa7cbfc988b58352001de9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:6865ada3f9be9adecdb91b3e1de7417f77715f513e659280b71f2c1846cad7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303073182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f08890e624437ca9667e894b93d4d0b18679e90e15c4a987220ba18c2cf1ead`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335e27b066f2c1c0bbeed39461a4a4fbf62a055865b375718b8f3b7829c7847`  
		Last Modified: Tue, 17 Sep 2024 01:57:46 GMT  
		Size: 145.6 MB (145550136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699c1af577d1d31fea174323154f98d80ebf0799a1653d1e16aa757dac2c0c5`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27537114c753be34bde0119da8822af92999c188c8179fae5d7818485ab1cc9`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cea4cf567c848a35ef033f3c580f5a9bb292d07e467b8b3fec2deb5b9ded5e`  
		Last Modified: Tue, 17 Sep 2024 01:57:46 GMT  
		Size: 126.1 MB (126080975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a45e091d1cf5d5b390d9186fbf47928cb8614e1a5e4c95c4c1d042010cdfc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1914764b74990c81519ecd791f43a90562a24488c06bd003f3989dbab719b95b`

```dockerfile
```

-	Layers:
	-	`sha256:9f7fef84eee0581296c386829208bb5a50f32d46fc94de3a2da8731bb14fe636`  
		Last Modified: Tue, 17 Sep 2024 01:57:45 GMT  
		Size: 3.0 MB (2993152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f576ad7926e77a49b4c68a367bc30414ad45aee426f6e47e6627bf2dbccb7fe6`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 19.6 KB (19590 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5114d2ce8cf864df0d46b61a83efc9091a8a9f541fd5a0552203f9f7a6b3bd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298486868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee3208ccef8bed14f5f24d2cfe75534065dc74ea62e33279b74c18454c46b57`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c14ea5bd28a65eb584dbc13e080a28deed5b2dfc84ae2658426304af8f58515`  
		Last Modified: Thu, 05 Sep 2024 07:57:40 GMT  
		Size: 142.4 MB (142354887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2c05e06974abd1044f3b0a63655c85405a56f40cfefdcee71e98502faab76`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20ff0775c7a1e3a4695b5d446055e4ab7f86102da49dc9c81c296a3bcd57c08`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bb011871fdbda36fb83ea88a689aa087392ca243e4d01d7f7e8a48716aa5c`  
		Last Modified: Thu, 05 Sep 2024 22:22:28 GMT  
		Size: 126.0 MB (126044198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bc9fb8fd6a2fc43d5ce841f8fc3800281c9336e2811bddf1013b15c7334b8788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d3d6d3248fcc7591237b1ce354f945e9c33e5e84bc811085eae0701df49b84`

```dockerfile
```

-	Layers:
	-	`sha256:c040a018d8d37b7b505f65b239525cd2b5220b784eddd8370ee92f94351a0195`  
		Last Modified: Thu, 05 Sep 2024 22:22:25 GMT  
		Size: 3.0 MB (2993988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8010ffea3ea7365cadcf5b422e457388d09feb73efdaa0734d0a1f097320ce93`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 20.1 KB (20143 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:f6cfefaf71a071c9ae79ff462df7c92fee795d3ebc189341c2ff657465feafaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2b7d52561db4c9b33cd5e871ebe89271b47ed5e86c190887b2ddd605e23be66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407242611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4381952cc5e93c6b589e3b862368611c3065332790aaa62dfb9343c253108ba6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cce711def6761647f11a49a3248a338024ef42471387ec25cb0c3ec1d5239a6 NEO4J_TARBALL=neo4j-enterprise-4.4.37-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922cdd1491a3cc027a8203ea9e12bb57b6ceab6066f62963506069a174f7b417`  
		Last Modified: Tue, 17 Sep 2024 01:57:51 GMT  
		Size: 145.6 MB (145550046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993f8a9c45a66cbbd96d6b659a44c0bf5d3b3748e5284323d8917aad4235aa04`  
		Last Modified: Tue, 17 Sep 2024 01:57:49 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09d8decb456d4e4ed9f4d3dd40e9df362853c1326813ed8bb2d7f49fd2a3aa`  
		Last Modified: Tue, 17 Sep 2024 01:57:49 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07a78e8ae22ea97da7fd76d225437eb61fec1ecaddf336ac51347d868873490`  
		Last Modified: Tue, 17 Sep 2024 01:57:52 GMT  
		Size: 230.3 MB (230250492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab82b4c2ad69f62533181e8e2d9e52be8242076d6b27e01e13b6241172bdf816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b9fe373c61a7cf877fa6b94a2338f4eb5f772163aee5e43e8630e5303b007c`

```dockerfile
```

-	Layers:
	-	`sha256:b030f4806c778ce4cee4b3bd8f074b2a6fe38ac5d3808defac40015b3e06610b`  
		Last Modified: Tue, 17 Sep 2024 01:57:49 GMT  
		Size: 3.1 MB (3132415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a711adc8dd95739d7b5f86f1268893f6b6640fd69d65dc6ae01d0c1aa1eace07`  
		Last Modified: Tue, 17 Sep 2024 01:57:49 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ec6bc788c5dacd3ddb1453b52493589a2b023c03a1e33cf83f580739f065da08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402657575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebddf2339582811ae515964afd7faa5ed7e3efb75068169340e85908899366f2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cce711def6761647f11a49a3248a338024ef42471387ec25cb0c3ec1d5239a6 NEO4J_TARBALL=neo4j-enterprise-4.4.37-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c14ea5bd28a65eb584dbc13e080a28deed5b2dfc84ae2658426304af8f58515`  
		Last Modified: Thu, 05 Sep 2024 07:57:40 GMT  
		Size: 142.4 MB (142354887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805ec3b229fba7572dea5134e35039051122b3d3e4cdb4f02694935b7a867d04`  
		Last Modified: Thu, 05 Sep 2024 22:23:37 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cef465729c419c19bda7077991cc8e39d3ac839d654844f15cfa8bc5d0020d`  
		Last Modified: Thu, 05 Sep 2024 22:23:37 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc0df68c835036821f7f0384647b789234099da49babd2664dfca305445be9`  
		Last Modified: Thu, 05 Sep 2024 22:23:43 GMT  
		Size: 230.2 MB (230214905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:dcad3320740072910b47bc261a662854c8b446f2292c913c01974111752028ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e6b15b1035b8e8ee5ca3391e465ed57c2184fa281d0c8ed4ffc7931322e960`

```dockerfile
```

-	Layers:
	-	`sha256:73ced3b366f7b107d17634210d447233a0f6634c123ddffd6217b2744b33b838`  
		Last Modified: Thu, 05 Sep 2024 22:23:37 GMT  
		Size: 3.1 MB (3133227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:393b13eac362381cba3c2a76fef6039cbfa99554687121913d86c4538ff7e3c0`  
		Last Modified: Thu, 05 Sep 2024 22:23:37 GMT  
		Size: 19.6 KB (19550 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37`

```console
$ docker pull neo4j@sha256:3fd0cb66f1de75d4451df1e05076e0a7098668b9acaa7cbfc988b58352001de9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37` - linux; amd64

```console
$ docker pull neo4j@sha256:6865ada3f9be9adecdb91b3e1de7417f77715f513e659280b71f2c1846cad7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303073182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f08890e624437ca9667e894b93d4d0b18679e90e15c4a987220ba18c2cf1ead`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335e27b066f2c1c0bbeed39461a4a4fbf62a055865b375718b8f3b7829c7847`  
		Last Modified: Tue, 17 Sep 2024 01:57:46 GMT  
		Size: 145.6 MB (145550136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699c1af577d1d31fea174323154f98d80ebf0799a1653d1e16aa757dac2c0c5`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27537114c753be34bde0119da8822af92999c188c8179fae5d7818485ab1cc9`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cea4cf567c848a35ef033f3c580f5a9bb292d07e467b8b3fec2deb5b9ded5e`  
		Last Modified: Tue, 17 Sep 2024 01:57:46 GMT  
		Size: 126.1 MB (126080975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a45e091d1cf5d5b390d9186fbf47928cb8614e1a5e4c95c4c1d042010cdfc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1914764b74990c81519ecd791f43a90562a24488c06bd003f3989dbab719b95b`

```dockerfile
```

-	Layers:
	-	`sha256:9f7fef84eee0581296c386829208bb5a50f32d46fc94de3a2da8731bb14fe636`  
		Last Modified: Tue, 17 Sep 2024 01:57:45 GMT  
		Size: 3.0 MB (2993152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f576ad7926e77a49b4c68a367bc30414ad45aee426f6e47e6627bf2dbccb7fe6`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 19.6 KB (19590 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5114d2ce8cf864df0d46b61a83efc9091a8a9f541fd5a0552203f9f7a6b3bd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298486868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee3208ccef8bed14f5f24d2cfe75534065dc74ea62e33279b74c18454c46b57`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c14ea5bd28a65eb584dbc13e080a28deed5b2dfc84ae2658426304af8f58515`  
		Last Modified: Thu, 05 Sep 2024 07:57:40 GMT  
		Size: 142.4 MB (142354887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2c05e06974abd1044f3b0a63655c85405a56f40cfefdcee71e98502faab76`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20ff0775c7a1e3a4695b5d446055e4ab7f86102da49dc9c81c296a3bcd57c08`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bb011871fdbda36fb83ea88a689aa087392ca243e4d01d7f7e8a48716aa5c`  
		Last Modified: Thu, 05 Sep 2024 22:22:28 GMT  
		Size: 126.0 MB (126044198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37` - unknown; unknown

```console
$ docker pull neo4j@sha256:bc9fb8fd6a2fc43d5ce841f8fc3800281c9336e2811bddf1013b15c7334b8788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d3d6d3248fcc7591237b1ce354f945e9c33e5e84bc811085eae0701df49b84`

```dockerfile
```

-	Layers:
	-	`sha256:c040a018d8d37b7b505f65b239525cd2b5220b784eddd8370ee92f94351a0195`  
		Last Modified: Thu, 05 Sep 2024 22:22:25 GMT  
		Size: 3.0 MB (2993988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8010ffea3ea7365cadcf5b422e457388d09feb73efdaa0734d0a1f097320ce93`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 20.1 KB (20143 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37-community`

```console
$ docker pull neo4j@sha256:3fd0cb66f1de75d4451df1e05076e0a7098668b9acaa7cbfc988b58352001de9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37-community` - linux; amd64

```console
$ docker pull neo4j@sha256:6865ada3f9be9adecdb91b3e1de7417f77715f513e659280b71f2c1846cad7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303073182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f08890e624437ca9667e894b93d4d0b18679e90e15c4a987220ba18c2cf1ead`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8335e27b066f2c1c0bbeed39461a4a4fbf62a055865b375718b8f3b7829c7847`  
		Last Modified: Tue, 17 Sep 2024 01:57:46 GMT  
		Size: 145.6 MB (145550136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699c1af577d1d31fea174323154f98d80ebf0799a1653d1e16aa757dac2c0c5`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27537114c753be34bde0119da8822af92999c188c8179fae5d7818485ab1cc9`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cea4cf567c848a35ef033f3c580f5a9bb292d07e467b8b3fec2deb5b9ded5e`  
		Last Modified: Tue, 17 Sep 2024 01:57:46 GMT  
		Size: 126.1 MB (126080975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a45e091d1cf5d5b390d9186fbf47928cb8614e1a5e4c95c4c1d042010cdfc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1914764b74990c81519ecd791f43a90562a24488c06bd003f3989dbab719b95b`

```dockerfile
```

-	Layers:
	-	`sha256:9f7fef84eee0581296c386829208bb5a50f32d46fc94de3a2da8731bb14fe636`  
		Last Modified: Tue, 17 Sep 2024 01:57:45 GMT  
		Size: 3.0 MB (2993152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f576ad7926e77a49b4c68a367bc30414ad45aee426f6e47e6627bf2dbccb7fe6`  
		Last Modified: Tue, 17 Sep 2024 01:57:44 GMT  
		Size: 19.6 KB (19590 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5114d2ce8cf864df0d46b61a83efc9091a8a9f541fd5a0552203f9f7a6b3bd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298486868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee3208ccef8bed14f5f24d2cfe75534065dc74ea62e33279b74c18454c46b57`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c14ea5bd28a65eb584dbc13e080a28deed5b2dfc84ae2658426304af8f58515`  
		Last Modified: Thu, 05 Sep 2024 07:57:40 GMT  
		Size: 142.4 MB (142354887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2c05e06974abd1044f3b0a63655c85405a56f40cfefdcee71e98502faab76`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20ff0775c7a1e3a4695b5d446055e4ab7f86102da49dc9c81c296a3bcd57c08`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bb011871fdbda36fb83ea88a689aa087392ca243e4d01d7f7e8a48716aa5c`  
		Last Modified: Thu, 05 Sep 2024 22:22:28 GMT  
		Size: 126.0 MB (126044198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bc9fb8fd6a2fc43d5ce841f8fc3800281c9336e2811bddf1013b15c7334b8788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d3d6d3248fcc7591237b1ce354f945e9c33e5e84bc811085eae0701df49b84`

```dockerfile
```

-	Layers:
	-	`sha256:c040a018d8d37b7b505f65b239525cd2b5220b784eddd8370ee92f94351a0195`  
		Last Modified: Thu, 05 Sep 2024 22:22:25 GMT  
		Size: 3.0 MB (2993988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8010ffea3ea7365cadcf5b422e457388d09feb73efdaa0734d0a1f097320ce93`  
		Last Modified: Thu, 05 Sep 2024 22:22:24 GMT  
		Size: 20.1 KB (20143 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37-enterprise`

```console
$ docker pull neo4j@sha256:f6cfefaf71a071c9ae79ff462df7c92fee795d3ebc189341c2ff657465feafaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2b7d52561db4c9b33cd5e871ebe89271b47ed5e86c190887b2ddd605e23be66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407242611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4381952cc5e93c6b589e3b862368611c3065332790aaa62dfb9343c253108ba6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cce711def6761647f11a49a3248a338024ef42471387ec25cb0c3ec1d5239a6 NEO4J_TARBALL=neo4j-enterprise-4.4.37-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922cdd1491a3cc027a8203ea9e12bb57b6ceab6066f62963506069a174f7b417`  
		Last Modified: Tue, 17 Sep 2024 01:57:51 GMT  
		Size: 145.6 MB (145550046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993f8a9c45a66cbbd96d6b659a44c0bf5d3b3748e5284323d8917aad4235aa04`  
		Last Modified: Tue, 17 Sep 2024 01:57:49 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09d8decb456d4e4ed9f4d3dd40e9df362853c1326813ed8bb2d7f49fd2a3aa`  
		Last Modified: Tue, 17 Sep 2024 01:57:49 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07a78e8ae22ea97da7fd76d225437eb61fec1ecaddf336ac51347d868873490`  
		Last Modified: Tue, 17 Sep 2024 01:57:52 GMT  
		Size: 230.3 MB (230250492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab82b4c2ad69f62533181e8e2d9e52be8242076d6b27e01e13b6241172bdf816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b9fe373c61a7cf877fa6b94a2338f4eb5f772163aee5e43e8630e5303b007c`

```dockerfile
```

-	Layers:
	-	`sha256:b030f4806c778ce4cee4b3bd8f074b2a6fe38ac5d3808defac40015b3e06610b`  
		Last Modified: Tue, 17 Sep 2024 01:57:49 GMT  
		Size: 3.1 MB (3132415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a711adc8dd95739d7b5f86f1268893f6b6640fd69d65dc6ae01d0c1aa1eace07`  
		Last Modified: Tue, 17 Sep 2024 01:57:49 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ec6bc788c5dacd3ddb1453b52493589a2b023c03a1e33cf83f580739f065da08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402657575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebddf2339582811ae515964afd7faa5ed7e3efb75068169340e85908899366f2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cce711def6761647f11a49a3248a338024ef42471387ec25cb0c3ec1d5239a6 NEO4J_TARBALL=neo4j-enterprise-4.4.37-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c14ea5bd28a65eb584dbc13e080a28deed5b2dfc84ae2658426304af8f58515`  
		Last Modified: Thu, 05 Sep 2024 07:57:40 GMT  
		Size: 142.4 MB (142354887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805ec3b229fba7572dea5134e35039051122b3d3e4cdb4f02694935b7a867d04`  
		Last Modified: Thu, 05 Sep 2024 22:23:37 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cef465729c419c19bda7077991cc8e39d3ac839d654844f15cfa8bc5d0020d`  
		Last Modified: Thu, 05 Sep 2024 22:23:37 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc0df68c835036821f7f0384647b789234099da49babd2664dfca305445be9`  
		Last Modified: Thu, 05 Sep 2024 22:23:43 GMT  
		Size: 230.2 MB (230214905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:dcad3320740072910b47bc261a662854c8b446f2292c913c01974111752028ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e6b15b1035b8e8ee5ca3391e465ed57c2184fa281d0c8ed4ffc7931322e960`

```dockerfile
```

-	Layers:
	-	`sha256:73ced3b366f7b107d17634210d447233a0f6634c123ddffd6217b2744b33b838`  
		Last Modified: Thu, 05 Sep 2024 22:23:37 GMT  
		Size: 3.1 MB (3133227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:393b13eac362381cba3c2a76fef6039cbfa99554687121913d86c4538ff7e3c0`  
		Last Modified: Thu, 05 Sep 2024 22:23:37 GMT  
		Size: 19.6 KB (19550 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:22f416f39e2cf95b3bda8b37961aa01892994f3a1f42158cdb5e0ef7c4a4424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c20e3822c048781fdb6f68c751e9d05f37dc3c8056625a76df2ef812e156d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287201721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64712a0504883a57e3488f3204e33ab3137be7b6d09308a91e7226a5d967c89a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe04b5554b5f8688b15a24bcb52868038523b74d472238dbc6f905df3d20e`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 124.3 MB (124348667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:78f79ef5e16622273feeb7338c77fb39708348eb4a1baef88d573107e5b27fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee9b4e85c149e3c876ee2e1584d6cfff246fbbc82023110f8ba29a28613a3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7171e8b71b8ffac3aee132f075d9d2a86ece6e870f1910d494252164dd80c07f`  
		Last Modified: Wed, 11 Sep 2024 02:08:40 GMT  
		Size: 5.2 MB (5236398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e727146735830fff543e40d4d7755296555c0d44962bbe0104f79c57d6405c`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:82e54229ae40cb806cc94c09508e8a721dc8050c7a8f5702fc94ab0a9c80bd0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:180496309e3983fdfc549fe288ffa6623cba3ef4db9dfe030a74096d1da7b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab29c1cb25683e168827ddcb1cf462220790a42624c18ef296424cd8c591bb78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee8095158276907c4c2e9d3815948439c193ced99c16b200872863c537ade7`  
		Last Modified: Tue, 17 Sep 2024 01:58:01 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d161bb420a4465d311908f84c4eb00d042e6f5a17f8c0646fc07fcaa1988`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e5cd119b228fa2abf79867ed9fd6ee7266339345f7f73fe8db04972b7071f`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f66be7307ffc19b11a63b345136406403a093fa8c866f6be46d88db67341e9`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 410.5 MB (410499175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2822cd65201e3d48c19a11841505e3d354f711d741575f62777e4460a2399821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae0576ed4b7c0f3aa88cf56b58a9c9ffafb768df5721f6602dac24e93ca3a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8f61206dc73a6085b6663cd684c8126df0f8cb8e483ea3053f3388fdb5c4db`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.3 MB (3310001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6ddda4f095819cf794006850f876d31281352f19a48c86dc4800d446cc4de`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:83c34c0ec6888b845513f0f537b30923f6789bdc9f08e7914d36f3acb20e7477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584508398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa010ae9add420d4096b9a82c92f81b2f4c10030b249dcf3256856e04500f5f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1399f6e4ba06ac0bae7e1fccceb6de0838ff07032e98ae866c6ee16971770c`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d04af29691c0799839badc798019698eb078ba094dd5e7e5cb9c2ca6f7a59`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fbd7232c537980eff5ade4b1bd0fe623d436fef632de6aec9d85e9de3f7d`  
		Last Modified: Thu, 05 Sep 2024 12:32:21 GMT  
		Size: 410.5 MB (410461037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ed29e8b428dc2fdcb4fadb49c2f59f862c1c7786fa1c13d2b693077411208ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840e22c1fe3a4898eddfaab9e6e1c858667ae47bdb2edc3c5a771cbe26816da7`

```dockerfile
```

-	Layers:
	-	`sha256:4aa608c3a262574f5fef377d4be8918bc18cbad16bc41f029aa55207394d0bc5`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 3.3 MB (3310312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee4c814fe545d83beeabb1e1a4727d9120e9c2d3606d0e67747b7306f29f241`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:82e54229ae40cb806cc94c09508e8a721dc8050c7a8f5702fc94ab0a9c80bd0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:180496309e3983fdfc549fe288ffa6623cba3ef4db9dfe030a74096d1da7b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab29c1cb25683e168827ddcb1cf462220790a42624c18ef296424cd8c591bb78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee8095158276907c4c2e9d3815948439c193ced99c16b200872863c537ade7`  
		Last Modified: Tue, 17 Sep 2024 01:58:01 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d161bb420a4465d311908f84c4eb00d042e6f5a17f8c0646fc07fcaa1988`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e5cd119b228fa2abf79867ed9fd6ee7266339345f7f73fe8db04972b7071f`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f66be7307ffc19b11a63b345136406403a093fa8c866f6be46d88db67341e9`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 410.5 MB (410499175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2822cd65201e3d48c19a11841505e3d354f711d741575f62777e4460a2399821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae0576ed4b7c0f3aa88cf56b58a9c9ffafb768df5721f6602dac24e93ca3a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8f61206dc73a6085b6663cd684c8126df0f8cb8e483ea3053f3388fdb5c4db`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.3 MB (3310001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6ddda4f095819cf794006850f876d31281352f19a48c86dc4800d446cc4de`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:83c34c0ec6888b845513f0f537b30923f6789bdc9f08e7914d36f3acb20e7477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584508398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa010ae9add420d4096b9a82c92f81b2f4c10030b249dcf3256856e04500f5f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1399f6e4ba06ac0bae7e1fccceb6de0838ff07032e98ae866c6ee16971770c`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d04af29691c0799839badc798019698eb078ba094dd5e7e5cb9c2ca6f7a59`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fbd7232c537980eff5ade4b1bd0fe623d436fef632de6aec9d85e9de3f7d`  
		Last Modified: Thu, 05 Sep 2024 12:32:21 GMT  
		Size: 410.5 MB (410461037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ed29e8b428dc2fdcb4fadb49c2f59f862c1c7786fa1c13d2b693077411208ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840e22c1fe3a4898eddfaab9e6e1c858667ae47bdb2edc3c5a771cbe26816da7`

```dockerfile
```

-	Layers:
	-	`sha256:4aa608c3a262574f5fef377d4be8918bc18cbad16bc41f029aa55207394d0bc5`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 3.3 MB (3310312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee4c814fe545d83beeabb1e1a4727d9120e9c2d3606d0e67747b7306f29f241`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:ef08046147e8deccec981e036371495509974e0191e30d7cb656e1ad03a8ab82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:9510d28ab152a5fa71a1d7d7ebd9794189c47feb1e40ea9a0ea2e57e71e1d43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572111242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340d94462634e4d3c58097bfba9547eedfc65e08ba8692aa819081e17e527228`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb85a96fe950defb874559fa1af495ffcc92e4cb64b42840c65689ca3c13976`  
		Last Modified: Wed, 11 Sep 2024 02:02:55 GMT  
		Size: 125.5 MB (125451252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11a4e92d6b55536bc70c5cc00712a5af2ad06a8b3a2b7e0b0ebb5e66ddf6ee3`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2cc6c3117344db03b0307f3353225e5c6323e9a68a4f040a0a9add27218a27`  
		Last Modified: Wed, 11 Sep 2024 02:02:59 GMT  
		Size: 407.6 MB (407567868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c441158911bae08a4484a187d71a04222c3a8622540512ff403295a36f6ec262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d93ae38b836bb9815c8dc7aebbf20651f32ae073c09b8efe4d55bbaa9089e`

```dockerfile
```

-	Layers:
	-	`sha256:20eb59f215c9170a99e6c3ca51b0ab5e507514d4a3e19df188eac6c0ec8aae70`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 5.5 MB (5537878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f18e49e1b6112f1b694fa51002a8158a532c4d9cd6e1f5da2a8be0837b555b`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 20.6 KB (20582 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2c9492fac02b39201ff2277511b5dd59e1923244fbf517d9b74f0b508a4d531f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.4 MB (570420951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d14a5e99c96d5eacf777c9b3c74387499a61313ac626a0e7955d8b34f5a6b7f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796337ad14f476d11236f08a6f0d8be705104fe6892be7c22cb0bc0f5610411f`  
		Last Modified: Wed, 11 Sep 2024 02:10:00 GMT  
		Size: 407.6 MB (407567897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9571454b3e46a9ad28cf29aa6d9b6fe294c6863cf4644c11d8e114e2c26f765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4126b5ce560bfbf7c3d639c3811b4904cb0e4971ced0a4415b55ac09df7ab8cc`

```dockerfile
```

-	Layers:
	-	`sha256:8ae39ba189f04bf8d99b9863ace6961d8df2f9950495bbc650e3fc01668bfdc1`  
		Last Modified: Wed, 11 Sep 2024 02:09:50 GMT  
		Size: 5.5 MB (5517443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5abdb07688b5221ff50ad1f7f69f20be5a122fbbf1d870346c9173b21fb21fd1`  
		Last Modified: Wed, 11 Sep 2024 02:09:49 GMT  
		Size: 20.9 KB (20889 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:22f416f39e2cf95b3bda8b37961aa01892994f3a1f42158cdb5e0ef7c4a4424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c20e3822c048781fdb6f68c751e9d05f37dc3c8056625a76df2ef812e156d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287201721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64712a0504883a57e3488f3204e33ab3137be7b6d09308a91e7226a5d967c89a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe04b5554b5f8688b15a24bcb52868038523b74d472238dbc6f905df3d20e`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 124.3 MB (124348667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:78f79ef5e16622273feeb7338c77fb39708348eb4a1baef88d573107e5b27fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee9b4e85c149e3c876ee2e1584d6cfff246fbbc82023110f8ba29a28613a3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7171e8b71b8ffac3aee132f075d9d2a86ece6e870f1910d494252164dd80c07f`  
		Last Modified: Wed, 11 Sep 2024 02:08:40 GMT  
		Size: 5.2 MB (5236398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e727146735830fff543e40d4d7755296555c0d44962bbe0104f79c57d6405c`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-community`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-community` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-community-bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-community-ubi9`

```console
$ docker pull neo4j@sha256:22f416f39e2cf95b3bda8b37961aa01892994f3a1f42158cdb5e0ef7c4a4424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c20e3822c048781fdb6f68c751e9d05f37dc3c8056625a76df2ef812e156d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287201721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64712a0504883a57e3488f3204e33ab3137be7b6d09308a91e7226a5d967c89a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe04b5554b5f8688b15a24bcb52868038523b74d472238dbc6f905df3d20e`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 124.3 MB (124348667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:78f79ef5e16622273feeb7338c77fb39708348eb4a1baef88d573107e5b27fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee9b4e85c149e3c876ee2e1584d6cfff246fbbc82023110f8ba29a28613a3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7171e8b71b8ffac3aee132f075d9d2a86ece6e870f1910d494252164dd80c07f`  
		Last Modified: Wed, 11 Sep 2024 02:08:40 GMT  
		Size: 5.2 MB (5236398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e727146735830fff543e40d4d7755296555c0d44962bbe0104f79c57d6405c`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-enterprise`

```console
$ docker pull neo4j@sha256:82e54229ae40cb806cc94c09508e8a721dc8050c7a8f5702fc94ab0a9c80bd0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:180496309e3983fdfc549fe288ffa6623cba3ef4db9dfe030a74096d1da7b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab29c1cb25683e168827ddcb1cf462220790a42624c18ef296424cd8c591bb78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee8095158276907c4c2e9d3815948439c193ced99c16b200872863c537ade7`  
		Last Modified: Tue, 17 Sep 2024 01:58:01 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d161bb420a4465d311908f84c4eb00d042e6f5a17f8c0646fc07fcaa1988`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e5cd119b228fa2abf79867ed9fd6ee7266339345f7f73fe8db04972b7071f`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f66be7307ffc19b11a63b345136406403a093fa8c866f6be46d88db67341e9`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 410.5 MB (410499175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2822cd65201e3d48c19a11841505e3d354f711d741575f62777e4460a2399821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae0576ed4b7c0f3aa88cf56b58a9c9ffafb768df5721f6602dac24e93ca3a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8f61206dc73a6085b6663cd684c8126df0f8cb8e483ea3053f3388fdb5c4db`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.3 MB (3310001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6ddda4f095819cf794006850f876d31281352f19a48c86dc4800d446cc4de`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:83c34c0ec6888b845513f0f537b30923f6789bdc9f08e7914d36f3acb20e7477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584508398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa010ae9add420d4096b9a82c92f81b2f4c10030b249dcf3256856e04500f5f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1399f6e4ba06ac0bae7e1fccceb6de0838ff07032e98ae866c6ee16971770c`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d04af29691c0799839badc798019698eb078ba094dd5e7e5cb9c2ca6f7a59`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fbd7232c537980eff5ade4b1bd0fe623d436fef632de6aec9d85e9de3f7d`  
		Last Modified: Thu, 05 Sep 2024 12:32:21 GMT  
		Size: 410.5 MB (410461037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ed29e8b428dc2fdcb4fadb49c2f59f862c1c7786fa1c13d2b693077411208ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840e22c1fe3a4898eddfaab9e6e1c858667ae47bdb2edc3c5a771cbe26816da7`

```dockerfile
```

-	Layers:
	-	`sha256:4aa608c3a262574f5fef377d4be8918bc18cbad16bc41f029aa55207394d0bc5`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 3.3 MB (3310312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee4c814fe545d83beeabb1e1a4727d9120e9c2d3606d0e67747b7306f29f241`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:82e54229ae40cb806cc94c09508e8a721dc8050c7a8f5702fc94ab0a9c80bd0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:180496309e3983fdfc549fe288ffa6623cba3ef4db9dfe030a74096d1da7b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab29c1cb25683e168827ddcb1cf462220790a42624c18ef296424cd8c591bb78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee8095158276907c4c2e9d3815948439c193ced99c16b200872863c537ade7`  
		Last Modified: Tue, 17 Sep 2024 01:58:01 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d161bb420a4465d311908f84c4eb00d042e6f5a17f8c0646fc07fcaa1988`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e5cd119b228fa2abf79867ed9fd6ee7266339345f7f73fe8db04972b7071f`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f66be7307ffc19b11a63b345136406403a093fa8c866f6be46d88db67341e9`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 410.5 MB (410499175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2822cd65201e3d48c19a11841505e3d354f711d741575f62777e4460a2399821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae0576ed4b7c0f3aa88cf56b58a9c9ffafb768df5721f6602dac24e93ca3a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8f61206dc73a6085b6663cd684c8126df0f8cb8e483ea3053f3388fdb5c4db`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.3 MB (3310001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6ddda4f095819cf794006850f876d31281352f19a48c86dc4800d446cc4de`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:83c34c0ec6888b845513f0f537b30923f6789bdc9f08e7914d36f3acb20e7477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584508398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa010ae9add420d4096b9a82c92f81b2f4c10030b249dcf3256856e04500f5f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1399f6e4ba06ac0bae7e1fccceb6de0838ff07032e98ae866c6ee16971770c`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d04af29691c0799839badc798019698eb078ba094dd5e7e5cb9c2ca6f7a59`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fbd7232c537980eff5ade4b1bd0fe623d436fef632de6aec9d85e9de3f7d`  
		Last Modified: Thu, 05 Sep 2024 12:32:21 GMT  
		Size: 410.5 MB (410461037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ed29e8b428dc2fdcb4fadb49c2f59f862c1c7786fa1c13d2b693077411208ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840e22c1fe3a4898eddfaab9e6e1c858667ae47bdb2edc3c5a771cbe26816da7`

```dockerfile
```

-	Layers:
	-	`sha256:4aa608c3a262574f5fef377d4be8918bc18cbad16bc41f029aa55207394d0bc5`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 3.3 MB (3310312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee4c814fe545d83beeabb1e1a4727d9120e9c2d3606d0e67747b7306f29f241`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:ef08046147e8deccec981e036371495509974e0191e30d7cb656e1ad03a8ab82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:9510d28ab152a5fa71a1d7d7ebd9794189c47feb1e40ea9a0ea2e57e71e1d43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572111242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340d94462634e4d3c58097bfba9547eedfc65e08ba8692aa819081e17e527228`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb85a96fe950defb874559fa1af495ffcc92e4cb64b42840c65689ca3c13976`  
		Last Modified: Wed, 11 Sep 2024 02:02:55 GMT  
		Size: 125.5 MB (125451252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11a4e92d6b55536bc70c5cc00712a5af2ad06a8b3a2b7e0b0ebb5e66ddf6ee3`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2cc6c3117344db03b0307f3353225e5c6323e9a68a4f040a0a9add27218a27`  
		Last Modified: Wed, 11 Sep 2024 02:02:59 GMT  
		Size: 407.6 MB (407567868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c441158911bae08a4484a187d71a04222c3a8622540512ff403295a36f6ec262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d93ae38b836bb9815c8dc7aebbf20651f32ae073c09b8efe4d55bbaa9089e`

```dockerfile
```

-	Layers:
	-	`sha256:20eb59f215c9170a99e6c3ca51b0ab5e507514d4a3e19df188eac6c0ec8aae70`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 5.5 MB (5537878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f18e49e1b6112f1b694fa51002a8158a532c4d9cd6e1f5da2a8be0837b555b`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 20.6 KB (20582 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2c9492fac02b39201ff2277511b5dd59e1923244fbf517d9b74f0b508a4d531f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.4 MB (570420951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d14a5e99c96d5eacf777c9b3c74387499a61313ac626a0e7955d8b34f5a6b7f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796337ad14f476d11236f08a6f0d8be705104fe6892be7c22cb0bc0f5610411f`  
		Last Modified: Wed, 11 Sep 2024 02:10:00 GMT  
		Size: 407.6 MB (407567897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9571454b3e46a9ad28cf29aa6d9b6fe294c6863cf4644c11d8e114e2c26f765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4126b5ce560bfbf7c3d639c3811b4904cb0e4971ced0a4415b55ac09df7ab8cc`

```dockerfile
```

-	Layers:
	-	`sha256:8ae39ba189f04bf8d99b9863ace6961d8df2f9950495bbc650e3fc01668bfdc1`  
		Last Modified: Wed, 11 Sep 2024 02:09:50 GMT  
		Size: 5.5 MB (5517443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5abdb07688b5221ff50ad1f7f69f20be5a122fbbf1d870346c9173b21fb21fd1`  
		Last Modified: Wed, 11 Sep 2024 02:09:49 GMT  
		Size: 20.9 KB (20889 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-ubi9`

```console
$ docker pull neo4j@sha256:22f416f39e2cf95b3bda8b37961aa01892994f3a1f42158cdb5e0ef7c4a4424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c20e3822c048781fdb6f68c751e9d05f37dc3c8056625a76df2ef812e156d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287201721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64712a0504883a57e3488f3204e33ab3137be7b6d09308a91e7226a5d967c89a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe04b5554b5f8688b15a24bcb52868038523b74d472238dbc6f905df3d20e`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 124.3 MB (124348667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:78f79ef5e16622273feeb7338c77fb39708348eb4a1baef88d573107e5b27fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee9b4e85c149e3c876ee2e1584d6cfff246fbbc82023110f8ba29a28613a3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7171e8b71b8ffac3aee132f075d9d2a86ece6e870f1910d494252164dd80c07f`  
		Last Modified: Wed, 11 Sep 2024 02:08:40 GMT  
		Size: 5.2 MB (5236398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e727146735830fff543e40d4d7755296555c0d44962bbe0104f79c57d6405c`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-community`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-community-bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-community-ubi9`

```console
$ docker pull neo4j@sha256:22f416f39e2cf95b3bda8b37961aa01892994f3a1f42158cdb5e0ef7c4a4424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c20e3822c048781fdb6f68c751e9d05f37dc3c8056625a76df2ef812e156d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287201721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64712a0504883a57e3488f3204e33ab3137be7b6d09308a91e7226a5d967c89a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe04b5554b5f8688b15a24bcb52868038523b74d472238dbc6f905df3d20e`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 124.3 MB (124348667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:78f79ef5e16622273feeb7338c77fb39708348eb4a1baef88d573107e5b27fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee9b4e85c149e3c876ee2e1584d6cfff246fbbc82023110f8ba29a28613a3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7171e8b71b8ffac3aee132f075d9d2a86ece6e870f1910d494252164dd80c07f`  
		Last Modified: Wed, 11 Sep 2024 02:08:40 GMT  
		Size: 5.2 MB (5236398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e727146735830fff543e40d4d7755296555c0d44962bbe0104f79c57d6405c`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-enterprise`

```console
$ docker pull neo4j@sha256:82e54229ae40cb806cc94c09508e8a721dc8050c7a8f5702fc94ab0a9c80bd0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:180496309e3983fdfc549fe288ffa6623cba3ef4db9dfe030a74096d1da7b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab29c1cb25683e168827ddcb1cf462220790a42624c18ef296424cd8c591bb78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee8095158276907c4c2e9d3815948439c193ced99c16b200872863c537ade7`  
		Last Modified: Tue, 17 Sep 2024 01:58:01 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d161bb420a4465d311908f84c4eb00d042e6f5a17f8c0646fc07fcaa1988`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e5cd119b228fa2abf79867ed9fd6ee7266339345f7f73fe8db04972b7071f`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f66be7307ffc19b11a63b345136406403a093fa8c866f6be46d88db67341e9`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 410.5 MB (410499175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2822cd65201e3d48c19a11841505e3d354f711d741575f62777e4460a2399821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae0576ed4b7c0f3aa88cf56b58a9c9ffafb768df5721f6602dac24e93ca3a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8f61206dc73a6085b6663cd684c8126df0f8cb8e483ea3053f3388fdb5c4db`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.3 MB (3310001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6ddda4f095819cf794006850f876d31281352f19a48c86dc4800d446cc4de`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:83c34c0ec6888b845513f0f537b30923f6789bdc9f08e7914d36f3acb20e7477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584508398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa010ae9add420d4096b9a82c92f81b2f4c10030b249dcf3256856e04500f5f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1399f6e4ba06ac0bae7e1fccceb6de0838ff07032e98ae866c6ee16971770c`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d04af29691c0799839badc798019698eb078ba094dd5e7e5cb9c2ca6f7a59`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fbd7232c537980eff5ade4b1bd0fe623d436fef632de6aec9d85e9de3f7d`  
		Last Modified: Thu, 05 Sep 2024 12:32:21 GMT  
		Size: 410.5 MB (410461037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ed29e8b428dc2fdcb4fadb49c2f59f862c1c7786fa1c13d2b693077411208ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840e22c1fe3a4898eddfaab9e6e1c858667ae47bdb2edc3c5a771cbe26816da7`

```dockerfile
```

-	Layers:
	-	`sha256:4aa608c3a262574f5fef377d4be8918bc18cbad16bc41f029aa55207394d0bc5`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 3.3 MB (3310312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee4c814fe545d83beeabb1e1a4727d9120e9c2d3606d0e67747b7306f29f241`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:82e54229ae40cb806cc94c09508e8a721dc8050c7a8f5702fc94ab0a9c80bd0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:180496309e3983fdfc549fe288ffa6623cba3ef4db9dfe030a74096d1da7b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab29c1cb25683e168827ddcb1cf462220790a42624c18ef296424cd8c591bb78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee8095158276907c4c2e9d3815948439c193ced99c16b200872863c537ade7`  
		Last Modified: Tue, 17 Sep 2024 01:58:01 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d161bb420a4465d311908f84c4eb00d042e6f5a17f8c0646fc07fcaa1988`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e5cd119b228fa2abf79867ed9fd6ee7266339345f7f73fe8db04972b7071f`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f66be7307ffc19b11a63b345136406403a093fa8c866f6be46d88db67341e9`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 410.5 MB (410499175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2822cd65201e3d48c19a11841505e3d354f711d741575f62777e4460a2399821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae0576ed4b7c0f3aa88cf56b58a9c9ffafb768df5721f6602dac24e93ca3a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8f61206dc73a6085b6663cd684c8126df0f8cb8e483ea3053f3388fdb5c4db`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.3 MB (3310001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6ddda4f095819cf794006850f876d31281352f19a48c86dc4800d446cc4de`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:83c34c0ec6888b845513f0f537b30923f6789bdc9f08e7914d36f3acb20e7477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584508398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa010ae9add420d4096b9a82c92f81b2f4c10030b249dcf3256856e04500f5f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1399f6e4ba06ac0bae7e1fccceb6de0838ff07032e98ae866c6ee16971770c`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d04af29691c0799839badc798019698eb078ba094dd5e7e5cb9c2ca6f7a59`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fbd7232c537980eff5ade4b1bd0fe623d436fef632de6aec9d85e9de3f7d`  
		Last Modified: Thu, 05 Sep 2024 12:32:21 GMT  
		Size: 410.5 MB (410461037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ed29e8b428dc2fdcb4fadb49c2f59f862c1c7786fa1c13d2b693077411208ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840e22c1fe3a4898eddfaab9e6e1c858667ae47bdb2edc3c5a771cbe26816da7`

```dockerfile
```

-	Layers:
	-	`sha256:4aa608c3a262574f5fef377d4be8918bc18cbad16bc41f029aa55207394d0bc5`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 3.3 MB (3310312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee4c814fe545d83beeabb1e1a4727d9120e9c2d3606d0e67747b7306f29f241`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:ef08046147e8deccec981e036371495509974e0191e30d7cb656e1ad03a8ab82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:9510d28ab152a5fa71a1d7d7ebd9794189c47feb1e40ea9a0ea2e57e71e1d43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572111242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340d94462634e4d3c58097bfba9547eedfc65e08ba8692aa819081e17e527228`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb85a96fe950defb874559fa1af495ffcc92e4cb64b42840c65689ca3c13976`  
		Last Modified: Wed, 11 Sep 2024 02:02:55 GMT  
		Size: 125.5 MB (125451252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11a4e92d6b55536bc70c5cc00712a5af2ad06a8b3a2b7e0b0ebb5e66ddf6ee3`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2cc6c3117344db03b0307f3353225e5c6323e9a68a4f040a0a9add27218a27`  
		Last Modified: Wed, 11 Sep 2024 02:02:59 GMT  
		Size: 407.6 MB (407567868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c441158911bae08a4484a187d71a04222c3a8622540512ff403295a36f6ec262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d93ae38b836bb9815c8dc7aebbf20651f32ae073c09b8efe4d55bbaa9089e`

```dockerfile
```

-	Layers:
	-	`sha256:20eb59f215c9170a99e6c3ca51b0ab5e507514d4a3e19df188eac6c0ec8aae70`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 5.5 MB (5537878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f18e49e1b6112f1b694fa51002a8158a532c4d9cd6e1f5da2a8be0837b555b`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 20.6 KB (20582 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2c9492fac02b39201ff2277511b5dd59e1923244fbf517d9b74f0b508a4d531f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.4 MB (570420951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d14a5e99c96d5eacf777c9b3c74387499a61313ac626a0e7955d8b34f5a6b7f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796337ad14f476d11236f08a6f0d8be705104fe6892be7c22cb0bc0f5610411f`  
		Last Modified: Wed, 11 Sep 2024 02:10:00 GMT  
		Size: 407.6 MB (407567897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9571454b3e46a9ad28cf29aa6d9b6fe294c6863cf4644c11d8e114e2c26f765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4126b5ce560bfbf7c3d639c3811b4904cb0e4971ced0a4415b55ac09df7ab8cc`

```dockerfile
```

-	Layers:
	-	`sha256:8ae39ba189f04bf8d99b9863ace6961d8df2f9950495bbc650e3fc01668bfdc1`  
		Last Modified: Wed, 11 Sep 2024 02:09:50 GMT  
		Size: 5.5 MB (5517443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5abdb07688b5221ff50ad1f7f69f20be5a122fbbf1d870346c9173b21fb21fd1`  
		Last Modified: Wed, 11 Sep 2024 02:09:49 GMT  
		Size: 20.9 KB (20889 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-ubi9`

```console
$ docker pull neo4j@sha256:22f416f39e2cf95b3bda8b37961aa01892994f3a1f42158cdb5e0ef7c4a4424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c20e3822c048781fdb6f68c751e9d05f37dc3c8056625a76df2ef812e156d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287201721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64712a0504883a57e3488f3204e33ab3137be7b6d09308a91e7226a5d967c89a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe04b5554b5f8688b15a24bcb52868038523b74d472238dbc6f905df3d20e`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 124.3 MB (124348667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:78f79ef5e16622273feeb7338c77fb39708348eb4a1baef88d573107e5b27fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee9b4e85c149e3c876ee2e1584d6cfff246fbbc82023110f8ba29a28613a3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7171e8b71b8ffac3aee132f075d9d2a86ece6e870f1910d494252164dd80c07f`  
		Last Modified: Wed, 11 Sep 2024 02:08:40 GMT  
		Size: 5.2 MB (5236398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e727146735830fff543e40d4d7755296555c0d44962bbe0104f79c57d6405c`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:22f416f39e2cf95b3bda8b37961aa01892994f3a1f42158cdb5e0ef7c4a4424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c20e3822c048781fdb6f68c751e9d05f37dc3c8056625a76df2ef812e156d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287201721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64712a0504883a57e3488f3204e33ab3137be7b6d09308a91e7226a5d967c89a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe04b5554b5f8688b15a24bcb52868038523b74d472238dbc6f905df3d20e`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 124.3 MB (124348667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:78f79ef5e16622273feeb7338c77fb39708348eb4a1baef88d573107e5b27fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee9b4e85c149e3c876ee2e1584d6cfff246fbbc82023110f8ba29a28613a3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7171e8b71b8ffac3aee132f075d9d2a86ece6e870f1910d494252164dd80c07f`  
		Last Modified: Wed, 11 Sep 2024 02:08:40 GMT  
		Size: 5.2 MB (5236398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e727146735830fff543e40d4d7755296555c0d44962bbe0104f79c57d6405c`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:82e54229ae40cb806cc94c09508e8a721dc8050c7a8f5702fc94ab0a9c80bd0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:180496309e3983fdfc549fe288ffa6623cba3ef4db9dfe030a74096d1da7b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab29c1cb25683e168827ddcb1cf462220790a42624c18ef296424cd8c591bb78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee8095158276907c4c2e9d3815948439c193ced99c16b200872863c537ade7`  
		Last Modified: Tue, 17 Sep 2024 01:58:01 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d161bb420a4465d311908f84c4eb00d042e6f5a17f8c0646fc07fcaa1988`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e5cd119b228fa2abf79867ed9fd6ee7266339345f7f73fe8db04972b7071f`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f66be7307ffc19b11a63b345136406403a093fa8c866f6be46d88db67341e9`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 410.5 MB (410499175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2822cd65201e3d48c19a11841505e3d354f711d741575f62777e4460a2399821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae0576ed4b7c0f3aa88cf56b58a9c9ffafb768df5721f6602dac24e93ca3a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8f61206dc73a6085b6663cd684c8126df0f8cb8e483ea3053f3388fdb5c4db`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.3 MB (3310001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6ddda4f095819cf794006850f876d31281352f19a48c86dc4800d446cc4de`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:83c34c0ec6888b845513f0f537b30923f6789bdc9f08e7914d36f3acb20e7477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584508398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa010ae9add420d4096b9a82c92f81b2f4c10030b249dcf3256856e04500f5f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1399f6e4ba06ac0bae7e1fccceb6de0838ff07032e98ae866c6ee16971770c`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d04af29691c0799839badc798019698eb078ba094dd5e7e5cb9c2ca6f7a59`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fbd7232c537980eff5ade4b1bd0fe623d436fef632de6aec9d85e9de3f7d`  
		Last Modified: Thu, 05 Sep 2024 12:32:21 GMT  
		Size: 410.5 MB (410461037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ed29e8b428dc2fdcb4fadb49c2f59f862c1c7786fa1c13d2b693077411208ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840e22c1fe3a4898eddfaab9e6e1c858667ae47bdb2edc3c5a771cbe26816da7`

```dockerfile
```

-	Layers:
	-	`sha256:4aa608c3a262574f5fef377d4be8918bc18cbad16bc41f029aa55207394d0bc5`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 3.3 MB (3310312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee4c814fe545d83beeabb1e1a4727d9120e9c2d3606d0e67747b7306f29f241`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:82e54229ae40cb806cc94c09508e8a721dc8050c7a8f5702fc94ab0a9c80bd0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:180496309e3983fdfc549fe288ffa6623cba3ef4db9dfe030a74096d1da7b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab29c1cb25683e168827ddcb1cf462220790a42624c18ef296424cd8c591bb78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee8095158276907c4c2e9d3815948439c193ced99c16b200872863c537ade7`  
		Last Modified: Tue, 17 Sep 2024 01:58:01 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682d161bb420a4465d311908f84c4eb00d042e6f5a17f8c0646fc07fcaa1988`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e5cd119b228fa2abf79867ed9fd6ee7266339345f7f73fe8db04972b7071f`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f66be7307ffc19b11a63b345136406403a093fa8c866f6be46d88db67341e9`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 410.5 MB (410499175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2822cd65201e3d48c19a11841505e3d354f711d741575f62777e4460a2399821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae0576ed4b7c0f3aa88cf56b58a9c9ffafb768df5721f6602dac24e93ca3a7`

```dockerfile
```

-	Layers:
	-	`sha256:0f8f61206dc73a6085b6663cd684c8126df0f8cb8e483ea3053f3388fdb5c4db`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 3.3 MB (3310001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6ddda4f095819cf794006850f876d31281352f19a48c86dc4800d446cc4de`  
		Last Modified: Tue, 17 Sep 2024 01:57:59 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:83c34c0ec6888b845513f0f537b30923f6789bdc9f08e7914d36f3acb20e7477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584508398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa010ae9add420d4096b9a82c92f81b2f4c10030b249dcf3256856e04500f5f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1399f6e4ba06ac0bae7e1fccceb6de0838ff07032e98ae866c6ee16971770c`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d04af29691c0799839badc798019698eb078ba094dd5e7e5cb9c2ca6f7a59`  
		Last Modified: Thu, 05 Sep 2024 12:32:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c2fbd7232c537980eff5ade4b1bd0fe623d436fef632de6aec9d85e9de3f7d`  
		Last Modified: Thu, 05 Sep 2024 12:32:21 GMT  
		Size: 410.5 MB (410461037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ed29e8b428dc2fdcb4fadb49c2f59f862c1c7786fa1c13d2b693077411208ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840e22c1fe3a4898eddfaab9e6e1c858667ae47bdb2edc3c5a771cbe26816da7`

```dockerfile
```

-	Layers:
	-	`sha256:4aa608c3a262574f5fef377d4be8918bc18cbad16bc41f029aa55207394d0bc5`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 3.3 MB (3310312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee4c814fe545d83beeabb1e1a4727d9120e9c2d3606d0e67747b7306f29f241`  
		Last Modified: Thu, 05 Sep 2024 12:32:13 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:ef08046147e8deccec981e036371495509974e0191e30d7cb656e1ad03a8ab82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:9510d28ab152a5fa71a1d7d7ebd9794189c47feb1e40ea9a0ea2e57e71e1d43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572111242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340d94462634e4d3c58097bfba9547eedfc65e08ba8692aa819081e17e527228`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb85a96fe950defb874559fa1af495ffcc92e4cb64b42840c65689ca3c13976`  
		Last Modified: Wed, 11 Sep 2024 02:02:55 GMT  
		Size: 125.5 MB (125451252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11a4e92d6b55536bc70c5cc00712a5af2ad06a8b3a2b7e0b0ebb5e66ddf6ee3`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2cc6c3117344db03b0307f3353225e5c6323e9a68a4f040a0a9add27218a27`  
		Last Modified: Wed, 11 Sep 2024 02:02:59 GMT  
		Size: 407.6 MB (407567868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c441158911bae08a4484a187d71a04222c3a8622540512ff403295a36f6ec262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d93ae38b836bb9815c8dc7aebbf20651f32ae073c09b8efe4d55bbaa9089e`

```dockerfile
```

-	Layers:
	-	`sha256:20eb59f215c9170a99e6c3ca51b0ab5e507514d4a3e19df188eac6c0ec8aae70`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 5.5 MB (5537878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f18e49e1b6112f1b694fa51002a8158a532c4d9cd6e1f5da2a8be0837b555b`  
		Last Modified: Wed, 11 Sep 2024 02:02:53 GMT  
		Size: 20.6 KB (20582 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2c9492fac02b39201ff2277511b5dd59e1923244fbf517d9b74f0b508a4d531f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.4 MB (570420951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d14a5e99c96d5eacf777c9b3c74387499a61313ac626a0e7955d8b34f5a6b7f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796337ad14f476d11236f08a6f0d8be705104fe6892be7c22cb0bc0f5610411f`  
		Last Modified: Wed, 11 Sep 2024 02:10:00 GMT  
		Size: 407.6 MB (407567897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9571454b3e46a9ad28cf29aa6d9b6fe294c6863cf4644c11d8e114e2c26f765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4126b5ce560bfbf7c3d639c3811b4904cb0e4971ced0a4415b55ac09df7ab8cc`

```dockerfile
```

-	Layers:
	-	`sha256:8ae39ba189f04bf8d99b9863ace6961d8df2f9950495bbc650e3fc01668bfdc1`  
		Last Modified: Wed, 11 Sep 2024 02:09:50 GMT  
		Size: 5.5 MB (5517443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5abdb07688b5221ff50ad1f7f69f20be5a122fbbf1d870346c9173b21fb21fd1`  
		Last Modified: Wed, 11 Sep 2024 02:09:49 GMT  
		Size: 20.9 KB (20889 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:22f416f39e2cf95b3bda8b37961aa01892994f3a1f42158cdb5e0ef7c4a4424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c20e3822c048781fdb6f68c751e9d05f37dc3c8056625a76df2ef812e156d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287201721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64712a0504883a57e3488f3204e33ab3137be7b6d09308a91e7226a5d967c89a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c5f27dbc1ca27f5aaac2c4d36156ee379b2656e31dc30d68ce56dc9574414`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 125.5 MB (125506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43074d678d20c0e98f259a0789b2a26384f0e1e03e0d840d9c20357d2150a65f`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe04b5554b5f8688b15a24bcb52868038523b74d472238dbc6f905df3d20e`  
		Last Modified: Wed, 11 Sep 2024 02:08:42 GMT  
		Size: 124.3 MB (124348667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:78f79ef5e16622273feeb7338c77fb39708348eb4a1baef88d573107e5b27fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee9b4e85c149e3c876ee2e1584d6cfff246fbbc82023110f8ba29a28613a3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7171e8b71b8ffac3aee132f075d9d2a86ece6e870f1910d494252164dd80c07f`  
		Last Modified: Wed, 11 Sep 2024 02:08:40 GMT  
		Size: 5.2 MB (5236398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e727146735830fff543e40d4d7755296555c0d44962bbe0104f79c57d6405c`  
		Last Modified: Wed, 11 Sep 2024 02:08:39 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json
