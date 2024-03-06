<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.31`](#neo4j4431)
-	[`neo4j:4.4.31-community`](#neo4j4431-community)
-	[`neo4j:4.4.31-enterprise`](#neo4j4431-enterprise)
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
$ docker pull neo4j@sha256:39691a1707d53ff13805169f24213076dbd2a716a3cb239b1a5a9a1a9f2eb4ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:cb0b8f6269cc9b6ebf3f71cbc4e667149b98bd06a27bedb425e099aafea959e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297289172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8e8f3e2ebaf8370b1936b39c0bbae7d32ed291a7872c0343cb28ee131fcfc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296c4e07731f3de39cbc23de4900f7eec95e134f2ee4e7a0c53853f60618309f`  
		Last Modified: Wed, 06 Mar 2024 06:49:31 GMT  
		Size: 145.3 MB (145271494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f103459b5bfdfc75ff3c2c877667e612ebb95910f36bce5b37873351e34b4`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7accafea02ead19b1e88edba8eb0f91db64fb554bdd4d3b7c71c5f98228fe18a`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3632fabc96af6ed6f6dc0abb78e6dfa0fab50eaaf5cd2e77b3b29475acb14d72`  
		Last Modified: Wed, 06 Mar 2024 06:49:30 GMT  
		Size: 120.6 MB (120581968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:9dae869a38f8a326cb1f74e80bf2e9009ce164865d64675dbe6d6d9bc4b04cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df007bcb10809cb89d11e674f6cdcb998b3ad51b13a9f6fc3f3f25e0e04524dc`

```dockerfile
```

-	Layers:
	-	`sha256:63ab52ddd94fdcf94ca75e97d84f1a701151274281361f2648f3bfe8cc8235bc`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 2.9 MB (2937569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4662d3009e5085a143320ce6ba242cf8ca83f121b02c0914361c1ce82f050ff`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 20.3 KB (20319 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9704a924afac957464f02f232afef831fd304160387e50801121c53ff013b4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292636064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c7d6f39f40fc28e72680d8ae6e2cbfda7e4eb4dd875145f1269a27f0470b04`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
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
	-	`sha256:365a86c8238455fe069a13bb071ee2c9641d98d3be5d927f921d115b4120bbfd`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f485ad9db2fa397719bb21b59c79dabdc0037f21ee6582f150141efb983957e`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a6ecc968f06ddad98ceb8201f3e42f8bbb7b7ec45b49d5209fd215b1b1b0d`  
		Last Modified: Wed, 28 Feb 2024 21:55:26 GMT  
		Size: 120.5 MB (120545106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:a28cbf57cd102b4008c416e26d4ed83b91de5ad7ae8c4ec18afdbd37017d650b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c166ff293287a897e20202210c485f2fe5644592ffb84a4c9b9c84ee2a790c03`

```dockerfile
```

-	Layers:
	-	`sha256:5b868b532910e623a651da783288bf02803f683a88d049cec1012616dcc69c22`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 2.9 MB (2937789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51599569f627085612b13278cebe9bf48815fa367160f584030fcc2a42a5311`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:39691a1707d53ff13805169f24213076dbd2a716a3cb239b1a5a9a1a9f2eb4ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:cb0b8f6269cc9b6ebf3f71cbc4e667149b98bd06a27bedb425e099aafea959e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297289172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8e8f3e2ebaf8370b1936b39c0bbae7d32ed291a7872c0343cb28ee131fcfc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296c4e07731f3de39cbc23de4900f7eec95e134f2ee4e7a0c53853f60618309f`  
		Last Modified: Wed, 06 Mar 2024 06:49:31 GMT  
		Size: 145.3 MB (145271494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f103459b5bfdfc75ff3c2c877667e612ebb95910f36bce5b37873351e34b4`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7accafea02ead19b1e88edba8eb0f91db64fb554bdd4d3b7c71c5f98228fe18a`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3632fabc96af6ed6f6dc0abb78e6dfa0fab50eaaf5cd2e77b3b29475acb14d72`  
		Last Modified: Wed, 06 Mar 2024 06:49:30 GMT  
		Size: 120.6 MB (120581968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9dae869a38f8a326cb1f74e80bf2e9009ce164865d64675dbe6d6d9bc4b04cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df007bcb10809cb89d11e674f6cdcb998b3ad51b13a9f6fc3f3f25e0e04524dc`

```dockerfile
```

-	Layers:
	-	`sha256:63ab52ddd94fdcf94ca75e97d84f1a701151274281361f2648f3bfe8cc8235bc`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 2.9 MB (2937569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4662d3009e5085a143320ce6ba242cf8ca83f121b02c0914361c1ce82f050ff`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 20.3 KB (20319 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9704a924afac957464f02f232afef831fd304160387e50801121c53ff013b4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292636064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c7d6f39f40fc28e72680d8ae6e2cbfda7e4eb4dd875145f1269a27f0470b04`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
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
	-	`sha256:365a86c8238455fe069a13bb071ee2c9641d98d3be5d927f921d115b4120bbfd`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f485ad9db2fa397719bb21b59c79dabdc0037f21ee6582f150141efb983957e`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a6ecc968f06ddad98ceb8201f3e42f8bbb7b7ec45b49d5209fd215b1b1b0d`  
		Last Modified: Wed, 28 Feb 2024 21:55:26 GMT  
		Size: 120.5 MB (120545106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a28cbf57cd102b4008c416e26d4ed83b91de5ad7ae8c4ec18afdbd37017d650b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c166ff293287a897e20202210c485f2fe5644592ffb84a4c9b9c84ee2a790c03`

```dockerfile
```

-	Layers:
	-	`sha256:5b868b532910e623a651da783288bf02803f683a88d049cec1012616dcc69c22`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 2.9 MB (2937789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51599569f627085612b13278cebe9bf48815fa367160f584030fcc2a42a5311`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:a71dca2ca93ca902f93f2550d6d76fe7a46a470f4541101523cd3f5464a2c537
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7d8dadeced700d12ac3ac30ebed9a37f796186fc4cba0af424cbe0b72d198843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401118603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f3213e8d0a389f26269099f0a72758303e77011b6add3d2b38fcd290995253`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=51b1e2141412fcfe348c3bb07cb2ad46fb86b3bfe5fc226ce21066443a4ba639 NEO4J_TARBALL=neo4j-enterprise-4.4.31-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296c4e07731f3de39cbc23de4900f7eec95e134f2ee4e7a0c53853f60618309f`  
		Last Modified: Wed, 06 Mar 2024 06:49:31 GMT  
		Size: 145.3 MB (145271494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f103459b5bfdfc75ff3c2c877667e612ebb95910f36bce5b37873351e34b4`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7accafea02ead19b1e88edba8eb0f91db64fb554bdd4d3b7c71c5f98228fe18a`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57714c77089bfa6dd8930754ddbbe72a0db1d26b55d3f0e9c521acdc886d76d`  
		Last Modified: Wed, 06 Mar 2024 06:49:47 GMT  
		Size: 224.4 MB (224411399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:bc32a4b9ff47539edecb384e8d09d42a469d74f8bad45424782e44038cb6c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f02a923f1700a2beb2aeb521ab26efc8bd634f2307e300a745046501fdda35d`

```dockerfile
```

-	Layers:
	-	`sha256:045dc413d912bbce885e5a63c2b55e1fa7a9f2d6e293b74c6af42fbfd7371d2e`  
		Last Modified: Wed, 06 Mar 2024 06:49:42 GMT  
		Size: 3.1 MB (3066246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987ee283c305e128ffe3335ef93b6878338bb20897fe3d04288e46b50eff69b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:42 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:10cd97a61ba6c2ed97a774886ec3a36420902e8f88cf648c7c01aa8a28302a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 MB (396467903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744185bcb8a34e93dfdc338cd9f35e6e23482897d5d1f0fc75774d874ee19f37`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=51b1e2141412fcfe348c3bb07cb2ad46fb86b3bfe5fc226ce21066443a4ba639 NEO4J_TARBALL=neo4j-enterprise-4.4.31-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
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
	-	`sha256:2d4853f08a3dc0cd3fb61b47b2469e466a5a576c52ea2db315addc1eb282e3d4`  
		Last Modified: Wed, 28 Feb 2024 21:56:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076de45c315978d69eb436414a116f0a29e1b65fbbbf85d4289a917ae8cfb96f`  
		Last Modified: Wed, 28 Feb 2024 21:56:24 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c70a49410eb451e951c91458c652845f8f451b89ab15439acfec6b4567dd0`  
		Last Modified: Wed, 28 Feb 2024 21:56:31 GMT  
		Size: 224.4 MB (224376946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b8f085b4efaadeacea04dc440fe2a1b5b52043d684a17630b3e64de315fa5969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf5755bdb37679b2927faf65d606fbc2d1b3df50a7a8f00249e3ba9ed022da7`

```dockerfile
```

-	Layers:
	-	`sha256:1e420cb15ee9afce459cb14ba93d458a980d870119ce0f60138bdc838ce417d2`  
		Last Modified: Wed, 28 Feb 2024 21:56:25 GMT  
		Size: 3.1 MB (3066462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e87fe98a6d98501693c3b6c9c41556b3cc4f07773d5909c8509b191a5c6f010`  
		Last Modified: Wed, 28 Feb 2024 21:56:24 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.31`

```console
$ docker pull neo4j@sha256:39691a1707d53ff13805169f24213076dbd2a716a3cb239b1a5a9a1a9f2eb4ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.31` - linux; amd64

```console
$ docker pull neo4j@sha256:cb0b8f6269cc9b6ebf3f71cbc4e667149b98bd06a27bedb425e099aafea959e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297289172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8e8f3e2ebaf8370b1936b39c0bbae7d32ed291a7872c0343cb28ee131fcfc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296c4e07731f3de39cbc23de4900f7eec95e134f2ee4e7a0c53853f60618309f`  
		Last Modified: Wed, 06 Mar 2024 06:49:31 GMT  
		Size: 145.3 MB (145271494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f103459b5bfdfc75ff3c2c877667e612ebb95910f36bce5b37873351e34b4`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7accafea02ead19b1e88edba8eb0f91db64fb554bdd4d3b7c71c5f98228fe18a`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3632fabc96af6ed6f6dc0abb78e6dfa0fab50eaaf5cd2e77b3b29475acb14d72`  
		Last Modified: Wed, 06 Mar 2024 06:49:30 GMT  
		Size: 120.6 MB (120581968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.31` - unknown; unknown

```console
$ docker pull neo4j@sha256:9dae869a38f8a326cb1f74e80bf2e9009ce164865d64675dbe6d6d9bc4b04cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df007bcb10809cb89d11e674f6cdcb998b3ad51b13a9f6fc3f3f25e0e04524dc`

```dockerfile
```

-	Layers:
	-	`sha256:63ab52ddd94fdcf94ca75e97d84f1a701151274281361f2648f3bfe8cc8235bc`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 2.9 MB (2937569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4662d3009e5085a143320ce6ba242cf8ca83f121b02c0914361c1ce82f050ff`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 20.3 KB (20319 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.31` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9704a924afac957464f02f232afef831fd304160387e50801121c53ff013b4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292636064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c7d6f39f40fc28e72680d8ae6e2cbfda7e4eb4dd875145f1269a27f0470b04`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
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
	-	`sha256:365a86c8238455fe069a13bb071ee2c9641d98d3be5d927f921d115b4120bbfd`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f485ad9db2fa397719bb21b59c79dabdc0037f21ee6582f150141efb983957e`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a6ecc968f06ddad98ceb8201f3e42f8bbb7b7ec45b49d5209fd215b1b1b0d`  
		Last Modified: Wed, 28 Feb 2024 21:55:26 GMT  
		Size: 120.5 MB (120545106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.31` - unknown; unknown

```console
$ docker pull neo4j@sha256:a28cbf57cd102b4008c416e26d4ed83b91de5ad7ae8c4ec18afdbd37017d650b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c166ff293287a897e20202210c485f2fe5644592ffb84a4c9b9c84ee2a790c03`

```dockerfile
```

-	Layers:
	-	`sha256:5b868b532910e623a651da783288bf02803f683a88d049cec1012616dcc69c22`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 2.9 MB (2937789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51599569f627085612b13278cebe9bf48815fa367160f584030fcc2a42a5311`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.31-community`

```console
$ docker pull neo4j@sha256:39691a1707d53ff13805169f24213076dbd2a716a3cb239b1a5a9a1a9f2eb4ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.31-community` - linux; amd64

```console
$ docker pull neo4j@sha256:cb0b8f6269cc9b6ebf3f71cbc4e667149b98bd06a27bedb425e099aafea959e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297289172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de8e8f3e2ebaf8370b1936b39c0bbae7d32ed291a7872c0343cb28ee131fcfc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296c4e07731f3de39cbc23de4900f7eec95e134f2ee4e7a0c53853f60618309f`  
		Last Modified: Wed, 06 Mar 2024 06:49:31 GMT  
		Size: 145.3 MB (145271494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f103459b5bfdfc75ff3c2c877667e612ebb95910f36bce5b37873351e34b4`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7accafea02ead19b1e88edba8eb0f91db64fb554bdd4d3b7c71c5f98228fe18a`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3632fabc96af6ed6f6dc0abb78e6dfa0fab50eaaf5cd2e77b3b29475acb14d72`  
		Last Modified: Wed, 06 Mar 2024 06:49:30 GMT  
		Size: 120.6 MB (120581968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.31-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9dae869a38f8a326cb1f74e80bf2e9009ce164865d64675dbe6d6d9bc4b04cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df007bcb10809cb89d11e674f6cdcb998b3ad51b13a9f6fc3f3f25e0e04524dc`

```dockerfile
```

-	Layers:
	-	`sha256:63ab52ddd94fdcf94ca75e97d84f1a701151274281361f2648f3bfe8cc8235bc`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 2.9 MB (2937569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4662d3009e5085a143320ce6ba242cf8ca83f121b02c0914361c1ce82f050ff`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 20.3 KB (20319 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.31-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9704a924afac957464f02f232afef831fd304160387e50801121c53ff013b4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292636064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c7d6f39f40fc28e72680d8ae6e2cbfda7e4eb4dd875145f1269a27f0470b04`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
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
	-	`sha256:365a86c8238455fe069a13bb071ee2c9641d98d3be5d927f921d115b4120bbfd`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f485ad9db2fa397719bb21b59c79dabdc0037f21ee6582f150141efb983957e`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a6ecc968f06ddad98ceb8201f3e42f8bbb7b7ec45b49d5209fd215b1b1b0d`  
		Last Modified: Wed, 28 Feb 2024 21:55:26 GMT  
		Size: 120.5 MB (120545106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.31-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a28cbf57cd102b4008c416e26d4ed83b91de5ad7ae8c4ec18afdbd37017d650b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c166ff293287a897e20202210c485f2fe5644592ffb84a4c9b9c84ee2a790c03`

```dockerfile
```

-	Layers:
	-	`sha256:5b868b532910e623a651da783288bf02803f683a88d049cec1012616dcc69c22`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 2.9 MB (2937789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51599569f627085612b13278cebe9bf48815fa367160f584030fcc2a42a5311`  
		Last Modified: Wed, 28 Feb 2024 21:55:23 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.31-enterprise`

```console
$ docker pull neo4j@sha256:a71dca2ca93ca902f93f2550d6d76fe7a46a470f4541101523cd3f5464a2c537
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.31-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7d8dadeced700d12ac3ac30ebed9a37f796186fc4cba0af424cbe0b72d198843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401118603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f3213e8d0a389f26269099f0a72758303e77011b6add3d2b38fcd290995253`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=51b1e2141412fcfe348c3bb07cb2ad46fb86b3bfe5fc226ce21066443a4ba639 NEO4J_TARBALL=neo4j-enterprise-4.4.31-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296c4e07731f3de39cbc23de4900f7eec95e134f2ee4e7a0c53853f60618309f`  
		Last Modified: Wed, 06 Mar 2024 06:49:31 GMT  
		Size: 145.3 MB (145271494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f103459b5bfdfc75ff3c2c877667e612ebb95910f36bce5b37873351e34b4`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7accafea02ead19b1e88edba8eb0f91db64fb554bdd4d3b7c71c5f98228fe18a`  
		Last Modified: Wed, 06 Mar 2024 06:49:27 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57714c77089bfa6dd8930754ddbbe72a0db1d26b55d3f0e9c521acdc886d76d`  
		Last Modified: Wed, 06 Mar 2024 06:49:47 GMT  
		Size: 224.4 MB (224411399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.31-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:bc32a4b9ff47539edecb384e8d09d42a469d74f8bad45424782e44038cb6c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f02a923f1700a2beb2aeb521ab26efc8bd634f2307e300a745046501fdda35d`

```dockerfile
```

-	Layers:
	-	`sha256:045dc413d912bbce885e5a63c2b55e1fa7a9f2d6e293b74c6af42fbfd7371d2e`  
		Last Modified: Wed, 06 Mar 2024 06:49:42 GMT  
		Size: 3.1 MB (3066246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987ee283c305e128ffe3335ef93b6878338bb20897fe3d04288e46b50eff69b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:42 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.31-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:10cd97a61ba6c2ed97a774886ec3a36420902e8f88cf648c7c01aa8a28302a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 MB (396467903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744185bcb8a34e93dfdc338cd9f35e6e23482897d5d1f0fc75774d874ee19f37`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=51b1e2141412fcfe348c3bb07cb2ad46fb86b3bfe5fc226ce21066443a4ba639 NEO4J_TARBALL=neo4j-enterprise-4.4.31-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
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
	-	`sha256:2d4853f08a3dc0cd3fb61b47b2469e466a5a576c52ea2db315addc1eb282e3d4`  
		Last Modified: Wed, 28 Feb 2024 21:56:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076de45c315978d69eb436414a116f0a29e1b65fbbbf85d4289a917ae8cfb96f`  
		Last Modified: Wed, 28 Feb 2024 21:56:24 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c70a49410eb451e951c91458c652845f8f451b89ab15439acfec6b4567dd0`  
		Last Modified: Wed, 28 Feb 2024 21:56:31 GMT  
		Size: 224.4 MB (224376946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.31-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b8f085b4efaadeacea04dc440fe2a1b5b52043d684a17630b3e64de315fa5969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf5755bdb37679b2927faf65d606fbc2d1b3df50a7a8f00249e3ba9ed022da7`

```dockerfile
```

-	Layers:
	-	`sha256:1e420cb15ee9afce459cb14ba93d458a980d870119ce0f60138bdc838ce417d2`  
		Last Modified: Wed, 28 Feb 2024 21:56:25 GMT  
		Size: 3.1 MB (3066462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e87fe98a6d98501693c3b6c9c41556b3cc4f07773d5909c8509b191a5c6f010`  
		Last Modified: Wed, 28 Feb 2024 21:56:24 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:7f947d2c2e92aaf8f5075fc91319c9da5a45a729f147f527388ab456440fcf40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:000c12cd4000c64698fed49f663bb5eaf56d92068a0d61577e05f5c843c3f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725568761cff2396dd02a4c228af561aa0d7925c115dc8b0e44ec83cc021526`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c863239754c808f30aa8d04804c154f58fd607b1ab26486846b97e47a5f45`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09133507ed01222c2fc6b0aadc2bf94972cf3041d8502b3717edcd2963d8205`  
		Last Modified: Wed, 06 Mar 2024 06:49:29 GMT  
		Size: 389.3 MB (389324329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:406563fdf2fc928308d9cb2b95b0202c91772dc78008df8e3823e6f41ebcfa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706df02f29d6fc83dd935d6520855d0c1158924caeb744303d9e466d1f6fa6`

```dockerfile
```

-	Layers:
	-	`sha256:c178791e286b9975331013581a3ce9a21995a8a22cd54d7b30d2b83ac5d59d4e`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e3c6c4b4d901203629da354230500d7edb7696d05881a99baa496c8230d4398`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
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
$ docker pull neo4j@sha256:7f947d2c2e92aaf8f5075fc91319c9da5a45a729f147f527388ab456440fcf40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:000c12cd4000c64698fed49f663bb5eaf56d92068a0d61577e05f5c843c3f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725568761cff2396dd02a4c228af561aa0d7925c115dc8b0e44ec83cc021526`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c863239754c808f30aa8d04804c154f58fd607b1ab26486846b97e47a5f45`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09133507ed01222c2fc6b0aadc2bf94972cf3041d8502b3717edcd2963d8205`  
		Last Modified: Wed, 06 Mar 2024 06:49:29 GMT  
		Size: 389.3 MB (389324329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:406563fdf2fc928308d9cb2b95b0202c91772dc78008df8e3823e6f41ebcfa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706df02f29d6fc83dd935d6520855d0c1158924caeb744303d9e466d1f6fa6`

```dockerfile
```

-	Layers:
	-	`sha256:c178791e286b9975331013581a3ce9a21995a8a22cd54d7b30d2b83ac5d59d4e`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e3c6c4b4d901203629da354230500d7edb7696d05881a99baa496c8230d4398`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-community` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:7f947d2c2e92aaf8f5075fc91319c9da5a45a729f147f527388ab456440fcf40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:000c12cd4000c64698fed49f663bb5eaf56d92068a0d61577e05f5c843c3f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725568761cff2396dd02a4c228af561aa0d7925c115dc8b0e44ec83cc021526`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c863239754c808f30aa8d04804c154f58fd607b1ab26486846b97e47a5f45`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09133507ed01222c2fc6b0aadc2bf94972cf3041d8502b3717edcd2963d8205`  
		Last Modified: Wed, 06 Mar 2024 06:49:29 GMT  
		Size: 389.3 MB (389324329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:406563fdf2fc928308d9cb2b95b0202c91772dc78008df8e3823e6f41ebcfa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706df02f29d6fc83dd935d6520855d0c1158924caeb744303d9e466d1f6fa6`

```dockerfile
```

-	Layers:
	-	`sha256:c178791e286b9975331013581a3ce9a21995a8a22cd54d7b30d2b83ac5d59d4e`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e3c6c4b4d901203629da354230500d7edb7696d05881a99baa496c8230d4398`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
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
$ docker pull neo4j@sha256:7f947d2c2e92aaf8f5075fc91319c9da5a45a729f147f527388ab456440fcf40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:000c12cd4000c64698fed49f663bb5eaf56d92068a0d61577e05f5c843c3f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725568761cff2396dd02a4c228af561aa0d7925c115dc8b0e44ec83cc021526`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c863239754c808f30aa8d04804c154f58fd607b1ab26486846b97e47a5f45`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09133507ed01222c2fc6b0aadc2bf94972cf3041d8502b3717edcd2963d8205`  
		Last Modified: Wed, 06 Mar 2024 06:49:29 GMT  
		Size: 389.3 MB (389324329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:406563fdf2fc928308d9cb2b95b0202c91772dc78008df8e3823e6f41ebcfa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706df02f29d6fc83dd935d6520855d0c1158924caeb744303d9e466d1f6fa6`

```dockerfile
```

-	Layers:
	-	`sha256:c178791e286b9975331013581a3ce9a21995a8a22cd54d7b30d2b83ac5d59d4e`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e3c6c4b4d901203629da354230500d7edb7696d05881a99baa496c8230d4398`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:7f947d2c2e92aaf8f5075fc91319c9da5a45a729f147f527388ab456440fcf40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:000c12cd4000c64698fed49f663bb5eaf56d92068a0d61577e05f5c843c3f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725568761cff2396dd02a4c228af561aa0d7925c115dc8b0e44ec83cc021526`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c863239754c808f30aa8d04804c154f58fd607b1ab26486846b97e47a5f45`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09133507ed01222c2fc6b0aadc2bf94972cf3041d8502b3717edcd2963d8205`  
		Last Modified: Wed, 06 Mar 2024 06:49:29 GMT  
		Size: 389.3 MB (389324329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:406563fdf2fc928308d9cb2b95b0202c91772dc78008df8e3823e6f41ebcfa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706df02f29d6fc83dd935d6520855d0c1158924caeb744303d9e466d1f6fa6`

```dockerfile
```

-	Layers:
	-	`sha256:c178791e286b9975331013581a3ce9a21995a8a22cd54d7b30d2b83ac5d59d4e`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e3c6c4b4d901203629da354230500d7edb7696d05881a99baa496c8230d4398`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
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
$ docker pull neo4j@sha256:7f947d2c2e92aaf8f5075fc91319c9da5a45a729f147f527388ab456440fcf40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.17.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:000c12cd4000c64698fed49f663bb5eaf56d92068a0d61577e05f5c843c3f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725568761cff2396dd02a4c228af561aa0d7925c115dc8b0e44ec83cc021526`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c863239754c808f30aa8d04804c154f58fd607b1ab26486846b97e47a5f45`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09133507ed01222c2fc6b0aadc2bf94972cf3041d8502b3717edcd2963d8205`  
		Last Modified: Wed, 06 Mar 2024 06:49:29 GMT  
		Size: 389.3 MB (389324329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.17.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:406563fdf2fc928308d9cb2b95b0202c91772dc78008df8e3823e6f41ebcfa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706df02f29d6fc83dd935d6520855d0c1158924caeb744303d9e466d1f6fa6`

```dockerfile
```

-	Layers:
	-	`sha256:c178791e286b9975331013581a3ce9a21995a8a22cd54d7b30d2b83ac5d59d4e`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e3c6c4b4d901203629da354230500d7edb7696d05881a99baa496c8230d4398`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
$ docker pull neo4j@sha256:7f947d2c2e92aaf8f5075fc91319c9da5a45a729f147f527388ab456440fcf40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:000c12cd4000c64698fed49f663bb5eaf56d92068a0d61577e05f5c843c3f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725568761cff2396dd02a4c228af561aa0d7925c115dc8b0e44ec83cc021526`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c863239754c808f30aa8d04804c154f58fd607b1ab26486846b97e47a5f45`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09133507ed01222c2fc6b0aadc2bf94972cf3041d8502b3717edcd2963d8205`  
		Last Modified: Wed, 06 Mar 2024 06:49:29 GMT  
		Size: 389.3 MB (389324329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:406563fdf2fc928308d9cb2b95b0202c91772dc78008df8e3823e6f41ebcfa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706df02f29d6fc83dd935d6520855d0c1158924caeb744303d9e466d1f6fa6`

```dockerfile
```

-	Layers:
	-	`sha256:c178791e286b9975331013581a3ce9a21995a8a22cd54d7b30d2b83ac5d59d4e`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e3c6c4b4d901203629da354230500d7edb7696d05881a99baa496c8230d4398`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
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
$ docker pull neo4j@sha256:7f947d2c2e92aaf8f5075fc91319c9da5a45a729f147f527388ab456440fcf40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:000c12cd4000c64698fed49f663bb5eaf56d92068a0d61577e05f5c843c3f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725568761cff2396dd02a4c228af561aa0d7925c115dc8b0e44ec83cc021526`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c863239754c808f30aa8d04804c154f58fd607b1ab26486846b97e47a5f45`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09133507ed01222c2fc6b0aadc2bf94972cf3041d8502b3717edcd2963d8205`  
		Last Modified: Wed, 06 Mar 2024 06:49:29 GMT  
		Size: 389.3 MB (389324329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:406563fdf2fc928308d9cb2b95b0202c91772dc78008df8e3823e6f41ebcfa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706df02f29d6fc83dd935d6520855d0c1158924caeb744303d9e466d1f6fa6`

```dockerfile
```

-	Layers:
	-	`sha256:c178791e286b9975331013581a3ce9a21995a8a22cd54d7b30d2b83ac5d59d4e`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e3c6c4b4d901203629da354230500d7edb7696d05881a99baa496c8230d4398`  
		Last Modified: Wed, 06 Mar 2024 06:49:23 GMT  
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
$ docker pull neo4j@sha256:d3917020995bd02e9591a5b0ed164b7ac7a6c34e8b1d2d2b41ee53f7d8b0db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:484920e5c185d7a862fe41b97f745c1b837037dc6b8bd7dcd24037d3816a00e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c0f3494c3dc1a59f522c8bb1b40ccb9669e39708974f18cb7c040ecb091a7`
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
	-	`sha256:5ccc5e47ddc23bb6d52da0af14f58cb63894156a156cadd7c024f13a21e59b68`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 144.9 MB (144893044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e261a8c08ba613cd08be05b4094d14670b6ff0177babe21548bdb177389b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8f1f13167215693412474c9550887890591bfb661a947a6fac4bd76ec7efb`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52341c045a4e258bd4b9a7393e20a7a2cffdf542a03759e0f328bed321343604`  
		Last Modified: Wed, 06 Mar 2024 06:49:12 GMT  
		Size: 116.1 MB (116122160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:489a6abca7aaf1131a91375043af39927959df6086975914294bdbafdc185d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96849e152263ed6d72f1837966be3420d8acb61a864077aa48515bc6178eda58`

```dockerfile
```

-	Layers:
	-	`sha256:ec992f9da5044782af2614b564b206151f47ee3399c69c9d10e1689d88f9fa5b`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00003421d2776a17a2b0bb993a8019092c0419766cb10eeebb342fd5933b24b1`  
		Last Modified: Wed, 06 Mar 2024 06:49:10 GMT  
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
