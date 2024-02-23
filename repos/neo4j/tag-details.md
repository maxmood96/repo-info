<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.30`](#neo4j4430)
-	[`neo4j:4.4.30-community`](#neo4j4430-community)
-	[`neo4j:4.4.30-enterprise`](#neo4j4430-enterprise)
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
-	[`neo4j:5.17`](#neo4j517)
-	[`neo4j:5.17-bullseye`](#neo4j517-bullseye)
-	[`neo4j:5.17-community`](#neo4j517-community)
-	[`neo4j:5.17-community-bullseye`](#neo4j517-community-bullseye)
-	[`neo4j:5.17-community-ubi8`](#neo4j517-community-ubi8)
-	[`neo4j:5.17-community-ubi9`](#neo4j517-community-ubi9)
-	[`neo4j:5.17-enterprise`](#neo4j517-enterprise)
-	[`neo4j:5.17-enterprise-bullseye`](#neo4j517-enterprise-bullseye)
-	[`neo4j:5.17-enterprise-ubi8`](#neo4j517-enterprise-ubi8)
-	[`neo4j:5.17-enterprise-ubi9`](#neo4j517-enterprise-ubi9)
-	[`neo4j:5.17-ubi8`](#neo4j517-ubi8)
-	[`neo4j:5.17-ubi9`](#neo4j517-ubi9)
-	[`neo4j:5.17.0`](#neo4j5170)
-	[`neo4j:5.17.0-bullseye`](#neo4j5170-bullseye)
-	[`neo4j:5.17.0-community`](#neo4j5170-community)
-	[`neo4j:5.17.0-community-bullseye`](#neo4j5170-community-bullseye)
-	[`neo4j:5.17.0-community-ubi8`](#neo4j5170-community-ubi8)
-	[`neo4j:5.17.0-community-ubi9`](#neo4j5170-community-ubi9)
-	[`neo4j:5.17.0-enterprise`](#neo4j5170-enterprise)
-	[`neo4j:5.17.0-enterprise-bullseye`](#neo4j5170-enterprise-bullseye)
-	[`neo4j:5.17.0-enterprise-ubi8`](#neo4j5170-enterprise-ubi8)
-	[`neo4j:5.17.0-enterprise-ubi9`](#neo4j5170-enterprise-ubi9)
-	[`neo4j:5.17.0-ubi8`](#neo4j5170-ubi8)
-	[`neo4j:5.17.0-ubi9`](#neo4j5170-ubi9)
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
$ docker pull neo4j@sha256:fb0fc1f5aa680e30f299e266cd08948a347eb43fcb39d3242f2f1157f0e41552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:93fbb9ff278d3b7770b186d77b3aa1d3dd4e1b1e6817c422b07eb8d365d72d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297284887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87277dbda4a84c2082bc49a240380faaba1e2bf9feef9a68b171890da90bd0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba095a8cc0d4c47de210a416e31cfbffa52fa59c8d656264c2e132f3a815b41d`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 145.3 MB (145271081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac6bdf3a9a7a930745a4b8168349a0cc05fdec7f1f2abd52747d1b70c8b96b`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db21cae4b3ff6d0bcacd513b0b182ddd3d265fd1806e4ab200aa6c08960d3f`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7f9d46d6b68f8b2910da80214f71d826369c9ec7fa707568fbfc90a5374f2`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 120.6 MB (120578124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:85d0647e8edcda71655de869e1ad5201f74e83ab9701c81fe53ffc5eb59de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a29ac354704e1e586afbc98b35478dc723a5c4b5ff13eea3ae729adfc30df`

```dockerfile
```

-	Layers:
	-	`sha256:36b48bce98a026724b6f4198924fa5e42f8d00fbfd339f8dcae87d5fbc8edda4`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 2.6 MB (2575369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436861a1531ac40aacf9abaabd6217fa07fe2b652c590a79ba7fb0a3178f46cb`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7432f87c0b8f66becedeafda2550fcbde2aa9f0b02ffb1570ad195a6ed3cda4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292637369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6782da458c79113c9172b41b621db0ddd64dd7369eca38dae68ff0d77ff44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3c502d96fd2479b383266b072c076a0e921dfa9d164556c4a131cde0157d8`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 142.0 MB (142006561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59043251df8635232212cd56cc131580c17cefc7d4390497a608ceb270ae5df`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a07e0e9c1d0bd083909eb4ffe592d9110002935e83232e7daab008b9b5958f`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beb8db73494338d288af638ad7c498897bc625b9021bbbba26843b94ec7bb7`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 120.5 MB (120546437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:82d0a44eb5624d883f43ba4d65b0fb06a1d8fc061a8a84a1837fddffb4a14f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b34548709111ff6d86522ab8445d41fa8a80296c2bba2e7a48c9c6d1a31dea`

```dockerfile
```

-	Layers:
	-	`sha256:2aae811ecdfe97d76124752791a297c5337700c756e034f8fa9d32fd4b4207a2`  
		Last Modified: Fri, 16 Feb 2024 13:51:24 GMT  
		Size: 2.6 MB (2575695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b3e4338af6391dc0591f8feb525dfee8998edc7f2ee07088c4d754fe54ec8f`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 20.2 KB (20163 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:fb0fc1f5aa680e30f299e266cd08948a347eb43fcb39d3242f2f1157f0e41552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:93fbb9ff278d3b7770b186d77b3aa1d3dd4e1b1e6817c422b07eb8d365d72d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297284887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87277dbda4a84c2082bc49a240380faaba1e2bf9feef9a68b171890da90bd0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba095a8cc0d4c47de210a416e31cfbffa52fa59c8d656264c2e132f3a815b41d`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 145.3 MB (145271081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac6bdf3a9a7a930745a4b8168349a0cc05fdec7f1f2abd52747d1b70c8b96b`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db21cae4b3ff6d0bcacd513b0b182ddd3d265fd1806e4ab200aa6c08960d3f`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7f9d46d6b68f8b2910da80214f71d826369c9ec7fa707568fbfc90a5374f2`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 120.6 MB (120578124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:85d0647e8edcda71655de869e1ad5201f74e83ab9701c81fe53ffc5eb59de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a29ac354704e1e586afbc98b35478dc723a5c4b5ff13eea3ae729adfc30df`

```dockerfile
```

-	Layers:
	-	`sha256:36b48bce98a026724b6f4198924fa5e42f8d00fbfd339f8dcae87d5fbc8edda4`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 2.6 MB (2575369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436861a1531ac40aacf9abaabd6217fa07fe2b652c590a79ba7fb0a3178f46cb`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7432f87c0b8f66becedeafda2550fcbde2aa9f0b02ffb1570ad195a6ed3cda4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292637369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6782da458c79113c9172b41b621db0ddd64dd7369eca38dae68ff0d77ff44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3c502d96fd2479b383266b072c076a0e921dfa9d164556c4a131cde0157d8`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 142.0 MB (142006561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59043251df8635232212cd56cc131580c17cefc7d4390497a608ceb270ae5df`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a07e0e9c1d0bd083909eb4ffe592d9110002935e83232e7daab008b9b5958f`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beb8db73494338d288af638ad7c498897bc625b9021bbbba26843b94ec7bb7`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 120.5 MB (120546437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:82d0a44eb5624d883f43ba4d65b0fb06a1d8fc061a8a84a1837fddffb4a14f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b34548709111ff6d86522ab8445d41fa8a80296c2bba2e7a48c9c6d1a31dea`

```dockerfile
```

-	Layers:
	-	`sha256:2aae811ecdfe97d76124752791a297c5337700c756e034f8fa9d32fd4b4207a2`  
		Last Modified: Fri, 16 Feb 2024 13:51:24 GMT  
		Size: 2.6 MB (2575695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b3e4338af6391dc0591f8feb525dfee8998edc7f2ee07088c4d754fe54ec8f`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 20.2 KB (20163 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:ce008e8f02f866d605178f0aaf9ccf8bc1c679a50faaa9c88dcfae1f7a5115e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1eb5378fe207f8023517d5d5f2437a9ae578c6179c0d0917cf298f4c0f1df41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402499192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78253fdb59394bcc43890175dd867d337fd94fa54e332e16cb313a329ddbcf14`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e3b493682ef0c012693021016cdb635597ad66078e2459b34c1c802d451e43`  
		Last Modified: Fri, 16 Feb 2024 02:50:16 GMT  
		Size: 145.3 MB (145271122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b1435146d7bcae51d98da09c3a494e57b410965054f4a3e55f1dd7a8136855`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904cfccbb1af040ece603b2781a6c70bff35f72d6f65bb2293ccf9213280dfc0`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34c4b777c6507310d60d8beac64a9c7e025aef534d54754ceac3d10fcdc658`  
		Last Modified: Fri, 16 Feb 2024 02:50:17 GMT  
		Size: 225.8 MB (225792389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5a6b17e0e6bac4ddf8a7553329246cba8024a4d49fae0bee461bc0df420f26a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf49abdd843e37603ba4ac8c9f4c85828d203e1c4817d872782e2b4576d59653`

```dockerfile
```

-	Layers:
	-	`sha256:f1745c678b2a247549d0a861bd468cba537f77a4c7b1af9ae6445ac9baf8da81`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 2.7 MB (2698858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa96a8119e23c3e684bc45aff961afdc4842a746210ec7778fe93ee667f3ffe`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:172dd1eaaf18ac7107bc3bfe3563ba40e2efdeb72281f61c2bb4a4e764f216fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397846363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f596698459a84e31f7b6276ae811ab637370d310be151b377fa6099b7d714d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3c502d96fd2479b383266b072c076a0e921dfa9d164556c4a131cde0157d8`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 142.0 MB (142006561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190f74e627ce5e110c1f372b25c10a54f0c555bb872286559af59b5aaa9c45eb`  
		Last Modified: Fri, 16 Feb 2024 13:52:35 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc727d6385e2b85fc051be2094bea898d60a9c55814c9123b1152b66eb8a7d`  
		Last Modified: Fri, 16 Feb 2024 13:52:35 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d107368a07e46384592b9ac1d789aa5c7b3d7025d265135484c417cd47e91fce`  
		Last Modified: Fri, 16 Feb 2024 13:52:41 GMT  
		Size: 225.8 MB (225755444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7a3ee22bf9d70ac182d87a286a7c7adc49510b5c11f9f1d508d567fb03ae3030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f7b8519326b4da18e04776c1cb429b4aa675da7dfbc82fc666983d2f90120e`

```dockerfile
```

-	Layers:
	-	`sha256:021d19882899953eec11ed55b04ea9b7c2fa8a369383ab7abee1f6eee82ed7e4`  
		Last Modified: Fri, 16 Feb 2024 13:52:36 GMT  
		Size: 2.7 MB (2699180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e95bfab41c4b7a4cee7be842e89c482bb6a8ab7e79c7d2ad95c8a4bc7136ea`  
		Last Modified: Fri, 16 Feb 2024 13:52:35 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30`

```console
$ docker pull neo4j@sha256:fb0fc1f5aa680e30f299e266cd08948a347eb43fcb39d3242f2f1157f0e41552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30` - linux; amd64

```console
$ docker pull neo4j@sha256:93fbb9ff278d3b7770b186d77b3aa1d3dd4e1b1e6817c422b07eb8d365d72d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297284887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87277dbda4a84c2082bc49a240380faaba1e2bf9feef9a68b171890da90bd0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba095a8cc0d4c47de210a416e31cfbffa52fa59c8d656264c2e132f3a815b41d`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 145.3 MB (145271081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac6bdf3a9a7a930745a4b8168349a0cc05fdec7f1f2abd52747d1b70c8b96b`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db21cae4b3ff6d0bcacd513b0b182ddd3d265fd1806e4ab200aa6c08960d3f`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7f9d46d6b68f8b2910da80214f71d826369c9ec7fa707568fbfc90a5374f2`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 120.6 MB (120578124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30` - unknown; unknown

```console
$ docker pull neo4j@sha256:85d0647e8edcda71655de869e1ad5201f74e83ab9701c81fe53ffc5eb59de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a29ac354704e1e586afbc98b35478dc723a5c4b5ff13eea3ae729adfc30df`

```dockerfile
```

-	Layers:
	-	`sha256:36b48bce98a026724b6f4198924fa5e42f8d00fbfd339f8dcae87d5fbc8edda4`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 2.6 MB (2575369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436861a1531ac40aacf9abaabd6217fa07fe2b652c590a79ba7fb0a3178f46cb`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7432f87c0b8f66becedeafda2550fcbde2aa9f0b02ffb1570ad195a6ed3cda4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292637369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6782da458c79113c9172b41b621db0ddd64dd7369eca38dae68ff0d77ff44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3c502d96fd2479b383266b072c076a0e921dfa9d164556c4a131cde0157d8`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 142.0 MB (142006561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59043251df8635232212cd56cc131580c17cefc7d4390497a608ceb270ae5df`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a07e0e9c1d0bd083909eb4ffe592d9110002935e83232e7daab008b9b5958f`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beb8db73494338d288af638ad7c498897bc625b9021bbbba26843b94ec7bb7`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 120.5 MB (120546437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30` - unknown; unknown

```console
$ docker pull neo4j@sha256:82d0a44eb5624d883f43ba4d65b0fb06a1d8fc061a8a84a1837fddffb4a14f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b34548709111ff6d86522ab8445d41fa8a80296c2bba2e7a48c9c6d1a31dea`

```dockerfile
```

-	Layers:
	-	`sha256:2aae811ecdfe97d76124752791a297c5337700c756e034f8fa9d32fd4b4207a2`  
		Last Modified: Fri, 16 Feb 2024 13:51:24 GMT  
		Size: 2.6 MB (2575695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b3e4338af6391dc0591f8feb525dfee8998edc7f2ee07088c4d754fe54ec8f`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 20.2 KB (20163 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30-community`

```console
$ docker pull neo4j@sha256:fb0fc1f5aa680e30f299e266cd08948a347eb43fcb39d3242f2f1157f0e41552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30-community` - linux; amd64

```console
$ docker pull neo4j@sha256:93fbb9ff278d3b7770b186d77b3aa1d3dd4e1b1e6817c422b07eb8d365d72d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297284887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87277dbda4a84c2082bc49a240380faaba1e2bf9feef9a68b171890da90bd0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba095a8cc0d4c47de210a416e31cfbffa52fa59c8d656264c2e132f3a815b41d`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 145.3 MB (145271081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac6bdf3a9a7a930745a4b8168349a0cc05fdec7f1f2abd52747d1b70c8b96b`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db21cae4b3ff6d0bcacd513b0b182ddd3d265fd1806e4ab200aa6c08960d3f`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7f9d46d6b68f8b2910da80214f71d826369c9ec7fa707568fbfc90a5374f2`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 120.6 MB (120578124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:85d0647e8edcda71655de869e1ad5201f74e83ab9701c81fe53ffc5eb59de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a29ac354704e1e586afbc98b35478dc723a5c4b5ff13eea3ae729adfc30df`

```dockerfile
```

-	Layers:
	-	`sha256:36b48bce98a026724b6f4198924fa5e42f8d00fbfd339f8dcae87d5fbc8edda4`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 2.6 MB (2575369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436861a1531ac40aacf9abaabd6217fa07fe2b652c590a79ba7fb0a3178f46cb`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7432f87c0b8f66becedeafda2550fcbde2aa9f0b02ffb1570ad195a6ed3cda4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292637369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6782da458c79113c9172b41b621db0ddd64dd7369eca38dae68ff0d77ff44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3c502d96fd2479b383266b072c076a0e921dfa9d164556c4a131cde0157d8`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 142.0 MB (142006561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59043251df8635232212cd56cc131580c17cefc7d4390497a608ceb270ae5df`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a07e0e9c1d0bd083909eb4ffe592d9110002935e83232e7daab008b9b5958f`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91beb8db73494338d288af638ad7c498897bc625b9021bbbba26843b94ec7bb7`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 120.5 MB (120546437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:82d0a44eb5624d883f43ba4d65b0fb06a1d8fc061a8a84a1837fddffb4a14f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b34548709111ff6d86522ab8445d41fa8a80296c2bba2e7a48c9c6d1a31dea`

```dockerfile
```

-	Layers:
	-	`sha256:2aae811ecdfe97d76124752791a297c5337700c756e034f8fa9d32fd4b4207a2`  
		Last Modified: Fri, 16 Feb 2024 13:51:24 GMT  
		Size: 2.6 MB (2575695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b3e4338af6391dc0591f8feb525dfee8998edc7f2ee07088c4d754fe54ec8f`  
		Last Modified: Fri, 16 Feb 2024 13:51:23 GMT  
		Size: 20.2 KB (20163 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30-enterprise`

```console
$ docker pull neo4j@sha256:ce008e8f02f866d605178f0aaf9ccf8bc1c679a50faaa9c88dcfae1f7a5115e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1eb5378fe207f8023517d5d5f2437a9ae578c6179c0d0917cf298f4c0f1df41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402499192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78253fdb59394bcc43890175dd867d337fd94fa54e332e16cb313a329ddbcf14`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e3b493682ef0c012693021016cdb635597ad66078e2459b34c1c802d451e43`  
		Last Modified: Fri, 16 Feb 2024 02:50:16 GMT  
		Size: 145.3 MB (145271122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b1435146d7bcae51d98da09c3a494e57b410965054f4a3e55f1dd7a8136855`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904cfccbb1af040ece603b2781a6c70bff35f72d6f65bb2293ccf9213280dfc0`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34c4b777c6507310d60d8beac64a9c7e025aef534d54754ceac3d10fcdc658`  
		Last Modified: Fri, 16 Feb 2024 02:50:17 GMT  
		Size: 225.8 MB (225792389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5a6b17e0e6bac4ddf8a7553329246cba8024a4d49fae0bee461bc0df420f26a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf49abdd843e37603ba4ac8c9f4c85828d203e1c4817d872782e2b4576d59653`

```dockerfile
```

-	Layers:
	-	`sha256:f1745c678b2a247549d0a861bd468cba537f77a4c7b1af9ae6445ac9baf8da81`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 2.7 MB (2698858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa96a8119e23c3e684bc45aff961afdc4842a746210ec7778fe93ee667f3ffe`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:172dd1eaaf18ac7107bc3bfe3563ba40e2efdeb72281f61c2bb4a4e764f216fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397846363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f596698459a84e31f7b6276ae811ab637370d310be151b377fa6099b7d714d8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3c502d96fd2479b383266b072c076a0e921dfa9d164556c4a131cde0157d8`  
		Last Modified: Fri, 16 Feb 2024 13:51:27 GMT  
		Size: 142.0 MB (142006561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190f74e627ce5e110c1f372b25c10a54f0c555bb872286559af59b5aaa9c45eb`  
		Last Modified: Fri, 16 Feb 2024 13:52:35 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc727d6385e2b85fc051be2094bea898d60a9c55814c9123b1152b66eb8a7d`  
		Last Modified: Fri, 16 Feb 2024 13:52:35 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d107368a07e46384592b9ac1d789aa5c7b3d7025d265135484c417cd47e91fce`  
		Last Modified: Fri, 16 Feb 2024 13:52:41 GMT  
		Size: 225.8 MB (225755444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7a3ee22bf9d70ac182d87a286a7c7adc49510b5c11f9f1d508d567fb03ae3030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f7b8519326b4da18e04776c1cb429b4aa675da7dfbc82fc666983d2f90120e`

```dockerfile
```

-	Layers:
	-	`sha256:021d19882899953eec11ed55b04ea9b7c2fa8a369383ab7abee1f6eee82ed7e4`  
		Last Modified: Fri, 16 Feb 2024 13:52:36 GMT  
		Size: 2.7 MB (2699180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e95bfab41c4b7a4cee7be842e89c482bb6a8ab7e79c7d2ad95c8a4bc7136ea`  
		Last Modified: Fri, 16 Feb 2024 13:52:35 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:5adddde7d6fb1a2598c66279d6db3420fb6ff517a3e290c77bf4bf0e0bf041f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fb66d89917c321f01bb2f439f45a903b027b89da10fef9aabbc2f48761b2b3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565652635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de742837b59da5a5f560629f3b13e0887caabae9f17162ca75ff0fa190532`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9d5e2be717906c2458bbc22677f05818787303c4ed959383bdab2cfd855d`  
		Last Modified: Fri, 23 Feb 2024 18:51:28 GMT  
		Size: 144.9 MB (144892443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611bfbb17a4767a77883ce926153c234981659eb75e69138bf92540a6253501`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71d9894d883d7c569eddfbcc9c57373d439c4ad806a4b3813355c7b0eda09a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2842bcf78f7da6fe25e4288e68b3760cba5ee6dead8d6521f202280b2ab8fb`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 389.3 MB (389324396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a4547d3ed47b90b650a1043407f8f2723be9ce5fe17f846977f1e2ce921e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab065cbcfbced56250318e5a94330823084731630379d5e39f86746df4a8cf5`

```dockerfile
```

-	Layers:
	-	`sha256:c5c83d1af68881dd42d57a2482a3e9f026a95b625a54ad46dbf4ad49c1d9508a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9378dc462e8d6f2b24e3fc2e470a716bee4f6b94c8859ef1f20acb62940f24b8`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55974fd78ca63f85237e1bdd9cb6ef6d0725896aeae53161f5b578ffc9265aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6babaaaae64f34a33cdd0a470c11949ece1b3043f0e30b681af78c6dc16e13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0f9bd7b739ab507683f618f7338ba196af578c8d8be670a9a5251340e794d`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7134fcb88c318450109cffd95158d495f44bdc4462186ca46ccc06e29988e50`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866384a64cf68fa3437e32fc7778a797e850196c55f4f74dd07eec653609b8a9`  
		Last Modified: Fri, 23 Feb 2024 18:55:56 GMT  
		Size: 389.3 MB (389287103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7aed7132417d5eaa9a5083e0b65b7b266f01587cfd2d3bf1b17c97b179332e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9cd3a7b70f29e828888ac09caa15431eaf42301bfdb74748966b77fc918b0`

```dockerfile
```

-	Layers:
	-	`sha256:02593d342c08a012710689ef695e8f2c8582293908093c8d59d5bf0d0bfe7cce`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd04f329af39b0687b12a48ef2741a61b9e23480ddb8b5516439014ed0577571`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5adddde7d6fb1a2598c66279d6db3420fb6ff517a3e290c77bf4bf0e0bf041f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:fb66d89917c321f01bb2f439f45a903b027b89da10fef9aabbc2f48761b2b3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565652635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de742837b59da5a5f560629f3b13e0887caabae9f17162ca75ff0fa190532`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9d5e2be717906c2458bbc22677f05818787303c4ed959383bdab2cfd855d`  
		Last Modified: Fri, 23 Feb 2024 18:51:28 GMT  
		Size: 144.9 MB (144892443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611bfbb17a4767a77883ce926153c234981659eb75e69138bf92540a6253501`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71d9894d883d7c569eddfbcc9c57373d439c4ad806a4b3813355c7b0eda09a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2842bcf78f7da6fe25e4288e68b3760cba5ee6dead8d6521f202280b2ab8fb`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 389.3 MB (389324396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a4547d3ed47b90b650a1043407f8f2723be9ce5fe17f846977f1e2ce921e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab065cbcfbced56250318e5a94330823084731630379d5e39f86746df4a8cf5`

```dockerfile
```

-	Layers:
	-	`sha256:c5c83d1af68881dd42d57a2482a3e9f026a95b625a54ad46dbf4ad49c1d9508a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9378dc462e8d6f2b24e3fc2e470a716bee4f6b94c8859ef1f20acb62940f24b8`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55974fd78ca63f85237e1bdd9cb6ef6d0725896aeae53161f5b578ffc9265aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6babaaaae64f34a33cdd0a470c11949ece1b3043f0e30b681af78c6dc16e13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0f9bd7b739ab507683f618f7338ba196af578c8d8be670a9a5251340e794d`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7134fcb88c318450109cffd95158d495f44bdc4462186ca46ccc06e29988e50`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866384a64cf68fa3437e32fc7778a797e850196c55f4f74dd07eec653609b8a9`  
		Last Modified: Fri, 23 Feb 2024 18:55:56 GMT  
		Size: 389.3 MB (389287103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7aed7132417d5eaa9a5083e0b65b7b266f01587cfd2d3bf1b17c97b179332e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9cd3a7b70f29e828888ac09caa15431eaf42301bfdb74748966b77fc918b0`

```dockerfile
```

-	Layers:
	-	`sha256:02593d342c08a012710689ef695e8f2c8582293908093c8d59d5bf0d0bfe7cce`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd04f329af39b0687b12a48ef2741a61b9e23480ddb8b5516439014ed0577571`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:c2f24c55f0ea8bcc80934aa179f49918f444c156023c21ff0c0c48a923b95dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:904beb2ed79cdaa9e666223d372274cf51b44cafc5b4e07bd5799bdd100a85dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589269445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d00d9433bc176aff9e3e6b9ff21e1c7e1986cf7d9283cf319fd2824204d7edf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a49eb38151ca388fa80eb98e18c6f5ef85dcd8fb7315fa609c498120ad28d0`  
		Last Modified: Fri, 23 Feb 2024 18:51:57 GMT  
		Size: 163.6 MB (163577740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d4ccf8ca9d5b7d2322147d5b1be42e4716c4465516776ebfadbfb8e62e8dc7`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 9.7 KB (9656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9c83e68e904b7dc8f2fd3669ad25ad5b12cb95d576bcb94cb3cffc90d787e`  
		Last Modified: Fri, 23 Feb 2024 18:52:01 GMT  
		Size: 386.4 MB (386389914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:dca7566746c27041625a3be754241b214886d9e62c89b5b8a4b00529c9171c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11022639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a80c58be80ef10f3bc943a8e7bebdd2718fb9ade551cd06b13fe2511dec4c`

```dockerfile
```

-	Layers:
	-	`sha256:cad35efde588348e0debf23ac10130815b74fcbd073ae91b24227d4c206c02fc`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 11.0 MB (11002402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c6b5ac29d1d755218db21e6714ad1382fabf2ce3bee9152a09213fc3a80ebd`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d3ac955137b3de314a2c557dfbbfa41713e7594969586c81c1c1aa55ae987b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574768646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d47e8b70ec8b3c14c2794f5359d1f1fac35d4437a157a1f271ca2e1e24a858`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce38530574a0791c26c54af2213fd4d24c3d62b102f7ea8db8c9d039f289e7e`  
		Last Modified: Fri, 23 Feb 2024 19:00:52 GMT  
		Size: 386.4 MB (386389916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:9c21d7938ae4c954920e5012715ed28ae2f729ddfbca964c026a4b1be3f41ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10490618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e232450558a959f89225082823cb60af7f5fb04a7bc203b692e3a6797caef8`

```dockerfile
```

-	Layers:
	-	`sha256:0a5feb2e27d68574aa57f6c6db81f34a8173a0f41d7705b90b10cfc1453934c1`  
		Last Modified: Fri, 23 Feb 2024 19:00:44 GMT  
		Size: 10.5 MB (10470539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cc20a366bec1600c5bff7894f4252c39ee2388b19a00b856429003f45c5360`  
		Last Modified: Fri, 23 Feb 2024 19:00:43 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f4a5d6e454607ede046e96eb21122a5d66e81b024063f22abb2978a47b9f64a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ccb1ee370100eb18985fc22273d4713d7da3c03f38bc18b89dcb61c6d316a0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.1 MB (676132904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e05085587403b0c69c7397dee2d2670105099abbf925cb6470563e67eb9f6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea9f35d719b8986fb084c21f8df565d1f3b38cb00bab53a4cf7fc04011ed52`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 252.0 MB (252011964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf99163b8f3a7c45f905f73d8e91c73db237e07898e572361301efe73e43f5d`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9829bdf3c809f0f1d3e727e687fe527723b2f1ece231b641810ee8adfa446bcc`  
		Last Modified: Fri, 23 Feb 2024 18:51:56 GMT  
		Size: 386.4 MB (386389639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e3916714511cc13603ae1e383b04d60a8fffcb570f43397aea38cecd8b6b4cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13722704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe4ef69dfd63cf7db912d01bd0e38570b4e3952a74889c17814f910f187755`

```dockerfile
```

-	Layers:
	-	`sha256:646669a250069b3b2bbb5ab81ee7271519680c0089ece996e83a6410f41d85cb`  
		Last Modified: Fri, 23 Feb 2024 18:51:52 GMT  
		Size: 13.7 MB (13702741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4316664f66d12d3edf32cb303d6fbd6e2da017b34972c76e99f5a6073c20f494`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9d326da1011c9d36019b40ebe80a08cdae4ae1a66807a4dec7eeccb07e7d0b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.5 MB (667475135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82db0c22b7b49b9111609e9db96568b69802a24644f25765545221294122b17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4079f7a3f13239ba4e7d4a97e2e3b193be6700523aa4e469dc31a81127fcb01`  
		Last Modified: Fri, 23 Feb 2024 18:58:52 GMT  
		Size: 386.4 MB (386389645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:62591f21bb56eac783a50278f0cf8a7b081d322fa670ae4b4b72932c2834fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13615603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b690629f9e2e5d5132f7e8a0832e8f96434e2908160bc9b1e10464c04abca43`

```dockerfile
```

-	Layers:
	-	`sha256:6403bb678609276aada73532e28a48934d2f75c3301bc5888531dc0dce02e013`  
		Last Modified: Fri, 23 Feb 2024 18:58:44 GMT  
		Size: 13.6 MB (13595797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8307bca2c474b1b9a72ed3caae6900cf7c93d6f83d9b75b9945290ec6595d865`  
		Last Modified: Fri, 23 Feb 2024 18:58:43 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-bullseye`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-community`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-community-bullseye`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-community-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-community-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-enterprise`

```console
$ docker pull neo4j@sha256:5adddde7d6fb1a2598c66279d6db3420fb6ff517a3e290c77bf4bf0e0bf041f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fb66d89917c321f01bb2f439f45a903b027b89da10fef9aabbc2f48761b2b3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565652635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de742837b59da5a5f560629f3b13e0887caabae9f17162ca75ff0fa190532`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9d5e2be717906c2458bbc22677f05818787303c4ed959383bdab2cfd855d`  
		Last Modified: Fri, 23 Feb 2024 18:51:28 GMT  
		Size: 144.9 MB (144892443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611bfbb17a4767a77883ce926153c234981659eb75e69138bf92540a6253501`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71d9894d883d7c569eddfbcc9c57373d439c4ad806a4b3813355c7b0eda09a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2842bcf78f7da6fe25e4288e68b3760cba5ee6dead8d6521f202280b2ab8fb`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 389.3 MB (389324396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a4547d3ed47b90b650a1043407f8f2723be9ce5fe17f846977f1e2ce921e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab065cbcfbced56250318e5a94330823084731630379d5e39f86746df4a8cf5`

```dockerfile
```

-	Layers:
	-	`sha256:c5c83d1af68881dd42d57a2482a3e9f026a95b625a54ad46dbf4ad49c1d9508a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9378dc462e8d6f2b24e3fc2e470a716bee4f6b94c8859ef1f20acb62940f24b8`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55974fd78ca63f85237e1bdd9cb6ef6d0725896aeae53161f5b578ffc9265aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6babaaaae64f34a33cdd0a470c11949ece1b3043f0e30b681af78c6dc16e13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0f9bd7b739ab507683f618f7338ba196af578c8d8be670a9a5251340e794d`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7134fcb88c318450109cffd95158d495f44bdc4462186ca46ccc06e29988e50`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866384a64cf68fa3437e32fc7778a797e850196c55f4f74dd07eec653609b8a9`  
		Last Modified: Fri, 23 Feb 2024 18:55:56 GMT  
		Size: 389.3 MB (389287103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7aed7132417d5eaa9a5083e0b65b7b266f01587cfd2d3bf1b17c97b179332e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9cd3a7b70f29e828888ac09caa15431eaf42301bfdb74748966b77fc918b0`

```dockerfile
```

-	Layers:
	-	`sha256:02593d342c08a012710689ef695e8f2c8582293908093c8d59d5bf0d0bfe7cce`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd04f329af39b0687b12a48ef2741a61b9e23480ddb8b5516439014ed0577571`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5adddde7d6fb1a2598c66279d6db3420fb6ff517a3e290c77bf4bf0e0bf041f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:fb66d89917c321f01bb2f439f45a903b027b89da10fef9aabbc2f48761b2b3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565652635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de742837b59da5a5f560629f3b13e0887caabae9f17162ca75ff0fa190532`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9d5e2be717906c2458bbc22677f05818787303c4ed959383bdab2cfd855d`  
		Last Modified: Fri, 23 Feb 2024 18:51:28 GMT  
		Size: 144.9 MB (144892443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611bfbb17a4767a77883ce926153c234981659eb75e69138bf92540a6253501`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71d9894d883d7c569eddfbcc9c57373d439c4ad806a4b3813355c7b0eda09a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2842bcf78f7da6fe25e4288e68b3760cba5ee6dead8d6521f202280b2ab8fb`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 389.3 MB (389324396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a4547d3ed47b90b650a1043407f8f2723be9ce5fe17f846977f1e2ce921e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab065cbcfbced56250318e5a94330823084731630379d5e39f86746df4a8cf5`

```dockerfile
```

-	Layers:
	-	`sha256:c5c83d1af68881dd42d57a2482a3e9f026a95b625a54ad46dbf4ad49c1d9508a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9378dc462e8d6f2b24e3fc2e470a716bee4f6b94c8859ef1f20acb62940f24b8`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55974fd78ca63f85237e1bdd9cb6ef6d0725896aeae53161f5b578ffc9265aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6babaaaae64f34a33cdd0a470c11949ece1b3043f0e30b681af78c6dc16e13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0f9bd7b739ab507683f618f7338ba196af578c8d8be670a9a5251340e794d`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7134fcb88c318450109cffd95158d495f44bdc4462186ca46ccc06e29988e50`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866384a64cf68fa3437e32fc7778a797e850196c55f4f74dd07eec653609b8a9`  
		Last Modified: Fri, 23 Feb 2024 18:55:56 GMT  
		Size: 389.3 MB (389287103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7aed7132417d5eaa9a5083e0b65b7b266f01587cfd2d3bf1b17c97b179332e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9cd3a7b70f29e828888ac09caa15431eaf42301bfdb74748966b77fc918b0`

```dockerfile
```

-	Layers:
	-	`sha256:02593d342c08a012710689ef695e8f2c8582293908093c8d59d5bf0d0bfe7cce`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd04f329af39b0687b12a48ef2741a61b9e23480ddb8b5516439014ed0577571`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:c2f24c55f0ea8bcc80934aa179f49918f444c156023c21ff0c0c48a923b95dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:904beb2ed79cdaa9e666223d372274cf51b44cafc5b4e07bd5799bdd100a85dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589269445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d00d9433bc176aff9e3e6b9ff21e1c7e1986cf7d9283cf319fd2824204d7edf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a49eb38151ca388fa80eb98e18c6f5ef85dcd8fb7315fa609c498120ad28d0`  
		Last Modified: Fri, 23 Feb 2024 18:51:57 GMT  
		Size: 163.6 MB (163577740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d4ccf8ca9d5b7d2322147d5b1be42e4716c4465516776ebfadbfb8e62e8dc7`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 9.7 KB (9656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9c83e68e904b7dc8f2fd3669ad25ad5b12cb95d576bcb94cb3cffc90d787e`  
		Last Modified: Fri, 23 Feb 2024 18:52:01 GMT  
		Size: 386.4 MB (386389914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:dca7566746c27041625a3be754241b214886d9e62c89b5b8a4b00529c9171c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11022639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a80c58be80ef10f3bc943a8e7bebdd2718fb9ade551cd06b13fe2511dec4c`

```dockerfile
```

-	Layers:
	-	`sha256:cad35efde588348e0debf23ac10130815b74fcbd073ae91b24227d4c206c02fc`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 11.0 MB (11002402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c6b5ac29d1d755218db21e6714ad1382fabf2ce3bee9152a09213fc3a80ebd`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d3ac955137b3de314a2c557dfbbfa41713e7594969586c81c1c1aa55ae987b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574768646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d47e8b70ec8b3c14c2794f5359d1f1fac35d4437a157a1f271ca2e1e24a858`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce38530574a0791c26c54af2213fd4d24c3d62b102f7ea8db8c9d039f289e7e`  
		Last Modified: Fri, 23 Feb 2024 19:00:52 GMT  
		Size: 386.4 MB (386389916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:9c21d7938ae4c954920e5012715ed28ae2f729ddfbca964c026a4b1be3f41ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10490618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e232450558a959f89225082823cb60af7f5fb04a7bc203b692e3a6797caef8`

```dockerfile
```

-	Layers:
	-	`sha256:0a5feb2e27d68574aa57f6c6db81f34a8173a0f41d7705b90b10cfc1453934c1`  
		Last Modified: Fri, 23 Feb 2024 19:00:44 GMT  
		Size: 10.5 MB (10470539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cc20a366bec1600c5bff7894f4252c39ee2388b19a00b856429003f45c5360`  
		Last Modified: Fri, 23 Feb 2024 19:00:43 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f4a5d6e454607ede046e96eb21122a5d66e81b024063f22abb2978a47b9f64a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ccb1ee370100eb18985fc22273d4713d7da3c03f38bc18b89dcb61c6d316a0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.1 MB (676132904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e05085587403b0c69c7397dee2d2670105099abbf925cb6470563e67eb9f6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea9f35d719b8986fb084c21f8df565d1f3b38cb00bab53a4cf7fc04011ed52`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 252.0 MB (252011964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf99163b8f3a7c45f905f73d8e91c73db237e07898e572361301efe73e43f5d`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9829bdf3c809f0f1d3e727e687fe527723b2f1ece231b641810ee8adfa446bcc`  
		Last Modified: Fri, 23 Feb 2024 18:51:56 GMT  
		Size: 386.4 MB (386389639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e3916714511cc13603ae1e383b04d60a8fffcb570f43397aea38cecd8b6b4cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13722704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe4ef69dfd63cf7db912d01bd0e38570b4e3952a74889c17814f910f187755`

```dockerfile
```

-	Layers:
	-	`sha256:646669a250069b3b2bbb5ab81ee7271519680c0089ece996e83a6410f41d85cb`  
		Last Modified: Fri, 23 Feb 2024 18:51:52 GMT  
		Size: 13.7 MB (13702741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4316664f66d12d3edf32cb303d6fbd6e2da017b34972c76e99f5a6073c20f494`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9d326da1011c9d36019b40ebe80a08cdae4ae1a66807a4dec7eeccb07e7d0b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.5 MB (667475135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82db0c22b7b49b9111609e9db96568b69802a24644f25765545221294122b17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4079f7a3f13239ba4e7d4a97e2e3b193be6700523aa4e469dc31a81127fcb01`  
		Last Modified: Fri, 23 Feb 2024 18:58:52 GMT  
		Size: 386.4 MB (386389645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:62591f21bb56eac783a50278f0cf8a7b081d322fa670ae4b4b72932c2834fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13615603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b690629f9e2e5d5132f7e8a0832e8f96434e2908160bc9b1e10464c04abca43`

```dockerfile
```

-	Layers:
	-	`sha256:6403bb678609276aada73532e28a48934d2f75c3301bc5888531dc0dce02e013`  
		Last Modified: Fri, 23 Feb 2024 18:58:44 GMT  
		Size: 13.6 MB (13595797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8307bca2c474b1b9a72ed3caae6900cf7c93d6f83d9b75b9945290ec6595d865`  
		Last Modified: Fri, 23 Feb 2024 18:58:43 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-bullseye`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-community`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-community-bullseye`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-community-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-community-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-enterprise`

```console
$ docker pull neo4j@sha256:5adddde7d6fb1a2598c66279d6db3420fb6ff517a3e290c77bf4bf0e0bf041f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fb66d89917c321f01bb2f439f45a903b027b89da10fef9aabbc2f48761b2b3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565652635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de742837b59da5a5f560629f3b13e0887caabae9f17162ca75ff0fa190532`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9d5e2be717906c2458bbc22677f05818787303c4ed959383bdab2cfd855d`  
		Last Modified: Fri, 23 Feb 2024 18:51:28 GMT  
		Size: 144.9 MB (144892443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611bfbb17a4767a77883ce926153c234981659eb75e69138bf92540a6253501`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71d9894d883d7c569eddfbcc9c57373d439c4ad806a4b3813355c7b0eda09a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2842bcf78f7da6fe25e4288e68b3760cba5ee6dead8d6521f202280b2ab8fb`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 389.3 MB (389324396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a4547d3ed47b90b650a1043407f8f2723be9ce5fe17f846977f1e2ce921e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab065cbcfbced56250318e5a94330823084731630379d5e39f86746df4a8cf5`

```dockerfile
```

-	Layers:
	-	`sha256:c5c83d1af68881dd42d57a2482a3e9f026a95b625a54ad46dbf4ad49c1d9508a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9378dc462e8d6f2b24e3fc2e470a716bee4f6b94c8859ef1f20acb62940f24b8`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55974fd78ca63f85237e1bdd9cb6ef6d0725896aeae53161f5b578ffc9265aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6babaaaae64f34a33cdd0a470c11949ece1b3043f0e30b681af78c6dc16e13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0f9bd7b739ab507683f618f7338ba196af578c8d8be670a9a5251340e794d`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7134fcb88c318450109cffd95158d495f44bdc4462186ca46ccc06e29988e50`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866384a64cf68fa3437e32fc7778a797e850196c55f4f74dd07eec653609b8a9`  
		Last Modified: Fri, 23 Feb 2024 18:55:56 GMT  
		Size: 389.3 MB (389287103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7aed7132417d5eaa9a5083e0b65b7b266f01587cfd2d3bf1b17c97b179332e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9cd3a7b70f29e828888ac09caa15431eaf42301bfdb74748966b77fc918b0`

```dockerfile
```

-	Layers:
	-	`sha256:02593d342c08a012710689ef695e8f2c8582293908093c8d59d5bf0d0bfe7cce`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd04f329af39b0687b12a48ef2741a61b9e23480ddb8b5516439014ed0577571`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5adddde7d6fb1a2598c66279d6db3420fb6ff517a3e290c77bf4bf0e0bf041f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:fb66d89917c321f01bb2f439f45a903b027b89da10fef9aabbc2f48761b2b3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565652635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de742837b59da5a5f560629f3b13e0887caabae9f17162ca75ff0fa190532`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9d5e2be717906c2458bbc22677f05818787303c4ed959383bdab2cfd855d`  
		Last Modified: Fri, 23 Feb 2024 18:51:28 GMT  
		Size: 144.9 MB (144892443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611bfbb17a4767a77883ce926153c234981659eb75e69138bf92540a6253501`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71d9894d883d7c569eddfbcc9c57373d439c4ad806a4b3813355c7b0eda09a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2842bcf78f7da6fe25e4288e68b3760cba5ee6dead8d6521f202280b2ab8fb`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 389.3 MB (389324396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a4547d3ed47b90b650a1043407f8f2723be9ce5fe17f846977f1e2ce921e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab065cbcfbced56250318e5a94330823084731630379d5e39f86746df4a8cf5`

```dockerfile
```

-	Layers:
	-	`sha256:c5c83d1af68881dd42d57a2482a3e9f026a95b625a54ad46dbf4ad49c1d9508a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9378dc462e8d6f2b24e3fc2e470a716bee4f6b94c8859ef1f20acb62940f24b8`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55974fd78ca63f85237e1bdd9cb6ef6d0725896aeae53161f5b578ffc9265aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6babaaaae64f34a33cdd0a470c11949ece1b3043f0e30b681af78c6dc16e13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0f9bd7b739ab507683f618f7338ba196af578c8d8be670a9a5251340e794d`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7134fcb88c318450109cffd95158d495f44bdc4462186ca46ccc06e29988e50`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866384a64cf68fa3437e32fc7778a797e850196c55f4f74dd07eec653609b8a9`  
		Last Modified: Fri, 23 Feb 2024 18:55:56 GMT  
		Size: 389.3 MB (389287103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7aed7132417d5eaa9a5083e0b65b7b266f01587cfd2d3bf1b17c97b179332e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9cd3a7b70f29e828888ac09caa15431eaf42301bfdb74748966b77fc918b0`

```dockerfile
```

-	Layers:
	-	`sha256:02593d342c08a012710689ef695e8f2c8582293908093c8d59d5bf0d0bfe7cce`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd04f329af39b0687b12a48ef2741a61b9e23480ddb8b5516439014ed0577571`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:c2f24c55f0ea8bcc80934aa179f49918f444c156023c21ff0c0c48a923b95dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:904beb2ed79cdaa9e666223d372274cf51b44cafc5b4e07bd5799bdd100a85dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589269445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d00d9433bc176aff9e3e6b9ff21e1c7e1986cf7d9283cf319fd2824204d7edf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a49eb38151ca388fa80eb98e18c6f5ef85dcd8fb7315fa609c498120ad28d0`  
		Last Modified: Fri, 23 Feb 2024 18:51:57 GMT  
		Size: 163.6 MB (163577740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d4ccf8ca9d5b7d2322147d5b1be42e4716c4465516776ebfadbfb8e62e8dc7`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 9.7 KB (9656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9c83e68e904b7dc8f2fd3669ad25ad5b12cb95d576bcb94cb3cffc90d787e`  
		Last Modified: Fri, 23 Feb 2024 18:52:01 GMT  
		Size: 386.4 MB (386389914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:dca7566746c27041625a3be754241b214886d9e62c89b5b8a4b00529c9171c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11022639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a80c58be80ef10f3bc943a8e7bebdd2718fb9ade551cd06b13fe2511dec4c`

```dockerfile
```

-	Layers:
	-	`sha256:cad35efde588348e0debf23ac10130815b74fcbd073ae91b24227d4c206c02fc`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 11.0 MB (11002402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c6b5ac29d1d755218db21e6714ad1382fabf2ce3bee9152a09213fc3a80ebd`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d3ac955137b3de314a2c557dfbbfa41713e7594969586c81c1c1aa55ae987b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574768646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d47e8b70ec8b3c14c2794f5359d1f1fac35d4437a157a1f271ca2e1e24a858`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce38530574a0791c26c54af2213fd4d24c3d62b102f7ea8db8c9d039f289e7e`  
		Last Modified: Fri, 23 Feb 2024 19:00:52 GMT  
		Size: 386.4 MB (386389916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:9c21d7938ae4c954920e5012715ed28ae2f729ddfbca964c026a4b1be3f41ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10490618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e232450558a959f89225082823cb60af7f5fb04a7bc203b692e3a6797caef8`

```dockerfile
```

-	Layers:
	-	`sha256:0a5feb2e27d68574aa57f6c6db81f34a8173a0f41d7705b90b10cfc1453934c1`  
		Last Modified: Fri, 23 Feb 2024 19:00:44 GMT  
		Size: 10.5 MB (10470539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cc20a366bec1600c5bff7894f4252c39ee2388b19a00b856429003f45c5360`  
		Last Modified: Fri, 23 Feb 2024 19:00:43 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f4a5d6e454607ede046e96eb21122a5d66e81b024063f22abb2978a47b9f64a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ccb1ee370100eb18985fc22273d4713d7da3c03f38bc18b89dcb61c6d316a0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.1 MB (676132904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e05085587403b0c69c7397dee2d2670105099abbf925cb6470563e67eb9f6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea9f35d719b8986fb084c21f8df565d1f3b38cb00bab53a4cf7fc04011ed52`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 252.0 MB (252011964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf99163b8f3a7c45f905f73d8e91c73db237e07898e572361301efe73e43f5d`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9829bdf3c809f0f1d3e727e687fe527723b2f1ece231b641810ee8adfa446bcc`  
		Last Modified: Fri, 23 Feb 2024 18:51:56 GMT  
		Size: 386.4 MB (386389639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e3916714511cc13603ae1e383b04d60a8fffcb570f43397aea38cecd8b6b4cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13722704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe4ef69dfd63cf7db912d01bd0e38570b4e3952a74889c17814f910f187755`

```dockerfile
```

-	Layers:
	-	`sha256:646669a250069b3b2bbb5ab81ee7271519680c0089ece996e83a6410f41d85cb`  
		Last Modified: Fri, 23 Feb 2024 18:51:52 GMT  
		Size: 13.7 MB (13702741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4316664f66d12d3edf32cb303d6fbd6e2da017b34972c76e99f5a6073c20f494`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9d326da1011c9d36019b40ebe80a08cdae4ae1a66807a4dec7eeccb07e7d0b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.5 MB (667475135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82db0c22b7b49b9111609e9db96568b69802a24644f25765545221294122b17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4079f7a3f13239ba4e7d4a97e2e3b193be6700523aa4e469dc31a81127fcb01`  
		Last Modified: Fri, 23 Feb 2024 18:58:52 GMT  
		Size: 386.4 MB (386389645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:62591f21bb56eac783a50278f0cf8a7b081d322fa670ae4b4b72932c2834fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13615603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b690629f9e2e5d5132f7e8a0832e8f96434e2908160bc9b1e10464c04abca43`

```dockerfile
```

-	Layers:
	-	`sha256:6403bb678609276aada73532e28a48934d2f75c3301bc5888531dc0dce02e013`  
		Last Modified: Fri, 23 Feb 2024 18:58:44 GMT  
		Size: 13.6 MB (13595797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8307bca2c474b1b9a72ed3caae6900cf7c93d6f83d9b75b9945290ec6595d865`  
		Last Modified: Fri, 23 Feb 2024 18:58:43 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.17.0-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.17.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:5adddde7d6fb1a2598c66279d6db3420fb6ff517a3e290c77bf4bf0e0bf041f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fb66d89917c321f01bb2f439f45a903b027b89da10fef9aabbc2f48761b2b3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565652635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de742837b59da5a5f560629f3b13e0887caabae9f17162ca75ff0fa190532`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9d5e2be717906c2458bbc22677f05818787303c4ed959383bdab2cfd855d`  
		Last Modified: Fri, 23 Feb 2024 18:51:28 GMT  
		Size: 144.9 MB (144892443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611bfbb17a4767a77883ce926153c234981659eb75e69138bf92540a6253501`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71d9894d883d7c569eddfbcc9c57373d439c4ad806a4b3813355c7b0eda09a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2842bcf78f7da6fe25e4288e68b3760cba5ee6dead8d6521f202280b2ab8fb`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 389.3 MB (389324396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a4547d3ed47b90b650a1043407f8f2723be9ce5fe17f846977f1e2ce921e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab065cbcfbced56250318e5a94330823084731630379d5e39f86746df4a8cf5`

```dockerfile
```

-	Layers:
	-	`sha256:c5c83d1af68881dd42d57a2482a3e9f026a95b625a54ad46dbf4ad49c1d9508a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9378dc462e8d6f2b24e3fc2e470a716bee4f6b94c8859ef1f20acb62940f24b8`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55974fd78ca63f85237e1bdd9cb6ef6d0725896aeae53161f5b578ffc9265aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6babaaaae64f34a33cdd0a470c11949ece1b3043f0e30b681af78c6dc16e13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0f9bd7b739ab507683f618f7338ba196af578c8d8be670a9a5251340e794d`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7134fcb88c318450109cffd95158d495f44bdc4462186ca46ccc06e29988e50`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866384a64cf68fa3437e32fc7778a797e850196c55f4f74dd07eec653609b8a9`  
		Last Modified: Fri, 23 Feb 2024 18:55:56 GMT  
		Size: 389.3 MB (389287103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7aed7132417d5eaa9a5083e0b65b7b266f01587cfd2d3bf1b17c97b179332e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9cd3a7b70f29e828888ac09caa15431eaf42301bfdb74748966b77fc918b0`

```dockerfile
```

-	Layers:
	-	`sha256:02593d342c08a012710689ef695e8f2c8582293908093c8d59d5bf0d0bfe7cce`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd04f329af39b0687b12a48ef2741a61b9e23480ddb8b5516439014ed0577571`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5adddde7d6fb1a2598c66279d6db3420fb6ff517a3e290c77bf4bf0e0bf041f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:fb66d89917c321f01bb2f439f45a903b027b89da10fef9aabbc2f48761b2b3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565652635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de742837b59da5a5f560629f3b13e0887caabae9f17162ca75ff0fa190532`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9d5e2be717906c2458bbc22677f05818787303c4ed959383bdab2cfd855d`  
		Last Modified: Fri, 23 Feb 2024 18:51:28 GMT  
		Size: 144.9 MB (144892443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611bfbb17a4767a77883ce926153c234981659eb75e69138bf92540a6253501`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71d9894d883d7c569eddfbcc9c57373d439c4ad806a4b3813355c7b0eda09a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2842bcf78f7da6fe25e4288e68b3760cba5ee6dead8d6521f202280b2ab8fb`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 389.3 MB (389324396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a4547d3ed47b90b650a1043407f8f2723be9ce5fe17f846977f1e2ce921e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab065cbcfbced56250318e5a94330823084731630379d5e39f86746df4a8cf5`

```dockerfile
```

-	Layers:
	-	`sha256:c5c83d1af68881dd42d57a2482a3e9f026a95b625a54ad46dbf4ad49c1d9508a`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9378dc462e8d6f2b24e3fc2e470a716bee4f6b94c8859ef1f20acb62940f24b8`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55974fd78ca63f85237e1bdd9cb6ef6d0725896aeae53161f5b578ffc9265aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6babaaaae64f34a33cdd0a470c11949ece1b3043f0e30b681af78c6dc16e13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0f9bd7b739ab507683f618f7338ba196af578c8d8be670a9a5251340e794d`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7134fcb88c318450109cffd95158d495f44bdc4462186ca46ccc06e29988e50`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866384a64cf68fa3437e32fc7778a797e850196c55f4f74dd07eec653609b8a9`  
		Last Modified: Fri, 23 Feb 2024 18:55:56 GMT  
		Size: 389.3 MB (389287103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7aed7132417d5eaa9a5083e0b65b7b266f01587cfd2d3bf1b17c97b179332e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9cd3a7b70f29e828888ac09caa15431eaf42301bfdb74748966b77fc918b0`

```dockerfile
```

-	Layers:
	-	`sha256:02593d342c08a012710689ef695e8f2c8582293908093c8d59d5bf0d0bfe7cce`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd04f329af39b0687b12a48ef2741a61b9e23480ddb8b5516439014ed0577571`  
		Last Modified: Fri, 23 Feb 2024 18:55:48 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:c2f24c55f0ea8bcc80934aa179f49918f444c156023c21ff0c0c48a923b95dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:904beb2ed79cdaa9e666223d372274cf51b44cafc5b4e07bd5799bdd100a85dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589269445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d00d9433bc176aff9e3e6b9ff21e1c7e1986cf7d9283cf319fd2824204d7edf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a49eb38151ca388fa80eb98e18c6f5ef85dcd8fb7315fa609c498120ad28d0`  
		Last Modified: Fri, 23 Feb 2024 18:51:57 GMT  
		Size: 163.6 MB (163577740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d4ccf8ca9d5b7d2322147d5b1be42e4716c4465516776ebfadbfb8e62e8dc7`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 9.7 KB (9656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9c83e68e904b7dc8f2fd3669ad25ad5b12cb95d576bcb94cb3cffc90d787e`  
		Last Modified: Fri, 23 Feb 2024 18:52:01 GMT  
		Size: 386.4 MB (386389914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:dca7566746c27041625a3be754241b214886d9e62c89b5b8a4b00529c9171c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11022639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a80c58be80ef10f3bc943a8e7bebdd2718fb9ade551cd06b13fe2511dec4c`

```dockerfile
```

-	Layers:
	-	`sha256:cad35efde588348e0debf23ac10130815b74fcbd073ae91b24227d4c206c02fc`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 11.0 MB (11002402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c6b5ac29d1d755218db21e6714ad1382fabf2ce3bee9152a09213fc3a80ebd`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d3ac955137b3de314a2c557dfbbfa41713e7594969586c81c1c1aa55ae987b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574768646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d47e8b70ec8b3c14c2794f5359d1f1fac35d4437a157a1f271ca2e1e24a858`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce38530574a0791c26c54af2213fd4d24c3d62b102f7ea8db8c9d039f289e7e`  
		Last Modified: Fri, 23 Feb 2024 19:00:52 GMT  
		Size: 386.4 MB (386389916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:9c21d7938ae4c954920e5012715ed28ae2f729ddfbca964c026a4b1be3f41ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10490618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e232450558a959f89225082823cb60af7f5fb04a7bc203b692e3a6797caef8`

```dockerfile
```

-	Layers:
	-	`sha256:0a5feb2e27d68574aa57f6c6db81f34a8173a0f41d7705b90b10cfc1453934c1`  
		Last Modified: Fri, 23 Feb 2024 19:00:44 GMT  
		Size: 10.5 MB (10470539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cc20a366bec1600c5bff7894f4252c39ee2388b19a00b856429003f45c5360`  
		Last Modified: Fri, 23 Feb 2024 19:00:43 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f4a5d6e454607ede046e96eb21122a5d66e81b024063f22abb2978a47b9f64a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ccb1ee370100eb18985fc22273d4713d7da3c03f38bc18b89dcb61c6d316a0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.1 MB (676132904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e05085587403b0c69c7397dee2d2670105099abbf925cb6470563e67eb9f6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea9f35d719b8986fb084c21f8df565d1f3b38cb00bab53a4cf7fc04011ed52`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 252.0 MB (252011964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf99163b8f3a7c45f905f73d8e91c73db237e07898e572361301efe73e43f5d`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9829bdf3c809f0f1d3e727e687fe527723b2f1ece231b641810ee8adfa446bcc`  
		Last Modified: Fri, 23 Feb 2024 18:51:56 GMT  
		Size: 386.4 MB (386389639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e3916714511cc13603ae1e383b04d60a8fffcb570f43397aea38cecd8b6b4cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13722704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe4ef69dfd63cf7db912d01bd0e38570b4e3952a74889c17814f910f187755`

```dockerfile
```

-	Layers:
	-	`sha256:646669a250069b3b2bbb5ab81ee7271519680c0089ece996e83a6410f41d85cb`  
		Last Modified: Fri, 23 Feb 2024 18:51:52 GMT  
		Size: 13.7 MB (13702741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4316664f66d12d3edf32cb303d6fbd6e2da017b34972c76e99f5a6073c20f494`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9d326da1011c9d36019b40ebe80a08cdae4ae1a66807a4dec7eeccb07e7d0b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.5 MB (667475135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82db0c22b7b49b9111609e9db96568b69802a24644f25765545221294122b17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4079f7a3f13239ba4e7d4a97e2e3b193be6700523aa4e469dc31a81127fcb01`  
		Last Modified: Fri, 23 Feb 2024 18:58:52 GMT  
		Size: 386.4 MB (386389645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:62591f21bb56eac783a50278f0cf8a7b081d322fa670ae4b4b72932c2834fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13615603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b690629f9e2e5d5132f7e8a0832e8f96434e2908160bc9b1e10464c04abca43`

```dockerfile
```

-	Layers:
	-	`sha256:6403bb678609276aada73532e28a48934d2f75c3301bc5888531dc0dce02e013`  
		Last Modified: Fri, 23 Feb 2024 18:58:44 GMT  
		Size: 13.6 MB (13595797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8307bca2c474b1b9a72ed3caae6900cf7c93d6f83d9b75b9945290ec6595d865`  
		Last Modified: Fri, 23 Feb 2024 18:58:43 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:cabd566a3c6d2ebd029731bf346021096335864f6d4fc6207041d232d8088aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:a26529541aa0385917f1f4c7947d58d3c7405be67948922c05129625a5a38889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292450399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbb22f0bf4111a40647dd325ed9e587cf8fc2de4c8bec194008b37e9258ad5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac648f8039d4a2e5fa6de66fe12ca5bb87b860f643f077397181682fa348a8`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 144.9 MB (144892424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09d251525de0c9e393640f527e8f21d6c4ead7918f56afa4feeb82dc86e75b`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e87980a848a65645611014382a46dd5f48d384c3a674029c60de6ad4f77817`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16466c11b676c95cf187f99244095f02e60708cf49fb5ac7711c8adf345cf036`  
		Last Modified: Fri, 23 Feb 2024 18:51:12 GMT  
		Size: 116.1 MB (116122178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:972652f21e0c948ee2493fe07be06b1da465c3cf8cc241e5e176ee1ad72392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b8a71f789266835aaf77411f82af7822d948e8820b43bb1809e5e33168352c`

```dockerfile
```

-	Layers:
	-	`sha256:47e73cd148b9cc442dc7264a75f2be259cc882a1c8654ce13880731e5e516d2a`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b4d2924d93371a13e114571c6e70b9905f93b0b125065a0eea5418af48573`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc2ad2211acfd1fd9693ad8b6d7355c9ae42fbba1aadb7d47fad084c1ae545a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3359d74f4009686d8dcd1cc804a04e45b433bd38333642bfdcb916020e5697af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e3158eb2130b430a7e1170c575b82b493811fa2537c6268f89d4010973efe`  
		Last Modified: Fri, 16 Feb 2024 13:48:56 GMT  
		Size: 143.7 MB (143720378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f396145151da560824585a7b30bb6b689f6e17d1495a0d1314ea0d9a6ddd7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f15891d8756a7478c74db43c026cd7a235bd3b60d6d4bb0fe12969becb715`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 9.5 KB (9498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23ea2b743cf5d850dec67f5eaa68ab6fe42ee8cc5e7ac306f680d7534bd03b`  
		Last Modified: Fri, 23 Feb 2024 18:54:25 GMT  
		Size: 116.1 MB (116091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:578a388be18a1758d0aa1dd3512b7cd95582f60b87092ba77354d485b0ba3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb9af7587b8af8a554bd4684fe36fea102ae56512ed24452154aefd25e50372`

```dockerfile
```

-	Layers:
	-	`sha256:2272aa58ca7b6afb8dda1013673ecf305baab2b2cc194c7a2b49c96998e70f59`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0c4b7e1c60664215b4a37c115aa232639742745276e48e4e210237a930366d`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json
