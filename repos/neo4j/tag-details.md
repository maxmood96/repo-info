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
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.16`](#neo4j516)
-	[`neo4j:5.16-bullseye`](#neo4j516-bullseye)
-	[`neo4j:5.16-community`](#neo4j516-community)
-	[`neo4j:5.16-community-bullseye`](#neo4j516-community-bullseye)
-	[`neo4j:5.16-community-ubi8`](#neo4j516-community-ubi8)
-	[`neo4j:5.16-enterprise`](#neo4j516-enterprise)
-	[`neo4j:5.16-enterprise-bullseye`](#neo4j516-enterprise-bullseye)
-	[`neo4j:5.16-enterprise-ubi8`](#neo4j516-enterprise-ubi8)
-	[`neo4j:5.16-ubi8`](#neo4j516-ubi8)
-	[`neo4j:5.16.0`](#neo4j5160)
-	[`neo4j:5.16.0-bullseye`](#neo4j5160-bullseye)
-	[`neo4j:5.16.0-community`](#neo4j5160-community)
-	[`neo4j:5.16.0-community-bullseye`](#neo4j5160-community-bullseye)
-	[`neo4j:5.16.0-community-ubi8`](#neo4j5160-community-ubi8)
-	[`neo4j:5.16.0-enterprise`](#neo4j5160-enterprise)
-	[`neo4j:5.16.0-enterprise-bullseye`](#neo4j5160-enterprise-bullseye)
-	[`neo4j:5.16.0-enterprise-ubi8`](#neo4j5160-enterprise-ubi8)
-	[`neo4j:5.16.0-ubi8`](#neo4j5160-ubi8)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi8`](#neo4jcommunity-ubi8)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi8`](#neo4jenterprise-ubi8)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi8`](#neo4jubi8)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:bc346abba1c30e1ca5ec28bce8a43357adc36ab6676a37a6eeccca95a17206c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:8e8117463bbf8260dcc786199c6aca82d843a3303caa770af40ac7cdbb383a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297283825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f0e5bf22f38c7ecab84732bdf0d404f8f502e0da705588a8db1e562b26fbbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
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
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ba8b81e446fea91a71d7b2fedf1f36cc5371805b772f569db46b9ec56d0e3f`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f4d805e3863a14cf676a825d60665b3b79ef71cf57e052eae3aa9a1f0ec44f`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52662ced7be079ae200c9c69496a0a723df611902c21a3d6cfe47675aae532ff`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04061e659c5d58cda64e9b84e2f9f039fd89fc80eac502c3820a9313fb3c65c5`  
		Last Modified: Fri, 02 Feb 2024 08:55:41 GMT  
		Size: 120.6 MB (120581522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:dbf81d9ad2798cad67b81903373450655381231252c5331ef7d1a09ea579d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ead4a3eadc586db63f7eff80da603796de41ce17deb75c5fc496522703826c`

```dockerfile
```

-	Layers:
	-	`sha256:ed11e124eef5338302d9ad7b3ff28eb34ee5d9a6e85f6d5fff0570dbc7e4c1a6`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 2.5 MB (2480430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae4663ab8668ba62904fb38b5ef7dfeca749e46d051234de9bc54ff785ed00e`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c70f9adf6056e4f46be400894767706878d0c77a58b3c3b7f5708d3f80987ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c903f0dfc9a6b8865426906a1d548d3f8b57948a91b3647cf6ae281b4a476dfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9635450a52f740af5ea7bb2bf90de5b55f740afe251beca93580b7bc66267046`  
		Last Modified: Sat, 03 Feb 2024 08:48:14 GMT  
		Size: 142.0 MB (142006579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377e38cfc0cbac782a756f3807641d8bd6871d2e4f6e05ec9df59e3413b81ba`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1896ba3d19a9edcd88ce13702d3e564ed4aa3d48294adc8d55d3fd0bfec225e2`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7dd7b38234441bd61821708c067ee8dd89fb525b7df24b9e9fb721820b4781`  
		Last Modified: Sat, 03 Feb 2024 08:48:13 GMT  
		Size: 120.5 MB (120547507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:22ee18af9fab1b36ea5bac688c00856119551828d46ac350ae8c2203fa6708f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2698c74ae872d7af3c48f7534f5a3314b25eb59ecd68cf1a55cfa75e4554f69`

```dockerfile
```

-	Layers:
	-	`sha256:19dc38792a3e8964b747247b734adf7d5e38304d6d087b6f8ce2f052779d05a2`  
		Last Modified: Sat, 03 Feb 2024 08:48:11 GMT  
		Size: 2.5 MB (2483929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441b336f4dd7306c3f3c7c872d24b6a10b3e266451525e681c25a38d6fc15530`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 20.2 KB (20163 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:bc346abba1c30e1ca5ec28bce8a43357adc36ab6676a37a6eeccca95a17206c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:8e8117463bbf8260dcc786199c6aca82d843a3303caa770af40ac7cdbb383a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297283825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f0e5bf22f38c7ecab84732bdf0d404f8f502e0da705588a8db1e562b26fbbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
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
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ba8b81e446fea91a71d7b2fedf1f36cc5371805b772f569db46b9ec56d0e3f`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f4d805e3863a14cf676a825d60665b3b79ef71cf57e052eae3aa9a1f0ec44f`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52662ced7be079ae200c9c69496a0a723df611902c21a3d6cfe47675aae532ff`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04061e659c5d58cda64e9b84e2f9f039fd89fc80eac502c3820a9313fb3c65c5`  
		Last Modified: Fri, 02 Feb 2024 08:55:41 GMT  
		Size: 120.6 MB (120581522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:dbf81d9ad2798cad67b81903373450655381231252c5331ef7d1a09ea579d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ead4a3eadc586db63f7eff80da603796de41ce17deb75c5fc496522703826c`

```dockerfile
```

-	Layers:
	-	`sha256:ed11e124eef5338302d9ad7b3ff28eb34ee5d9a6e85f6d5fff0570dbc7e4c1a6`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 2.5 MB (2480430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae4663ab8668ba62904fb38b5ef7dfeca749e46d051234de9bc54ff785ed00e`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c70f9adf6056e4f46be400894767706878d0c77a58b3c3b7f5708d3f80987ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c903f0dfc9a6b8865426906a1d548d3f8b57948a91b3647cf6ae281b4a476dfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9635450a52f740af5ea7bb2bf90de5b55f740afe251beca93580b7bc66267046`  
		Last Modified: Sat, 03 Feb 2024 08:48:14 GMT  
		Size: 142.0 MB (142006579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377e38cfc0cbac782a756f3807641d8bd6871d2e4f6e05ec9df59e3413b81ba`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1896ba3d19a9edcd88ce13702d3e564ed4aa3d48294adc8d55d3fd0bfec225e2`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7dd7b38234441bd61821708c067ee8dd89fb525b7df24b9e9fb721820b4781`  
		Last Modified: Sat, 03 Feb 2024 08:48:13 GMT  
		Size: 120.5 MB (120547507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:22ee18af9fab1b36ea5bac688c00856119551828d46ac350ae8c2203fa6708f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2698c74ae872d7af3c48f7534f5a3314b25eb59ecd68cf1a55cfa75e4554f69`

```dockerfile
```

-	Layers:
	-	`sha256:19dc38792a3e8964b747247b734adf7d5e38304d6d087b6f8ce2f052779d05a2`  
		Last Modified: Sat, 03 Feb 2024 08:48:11 GMT  
		Size: 2.5 MB (2483929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441b336f4dd7306c3f3c7c872d24b6a10b3e266451525e681c25a38d6fc15530`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 20.2 KB (20163 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:fbc9da0af3c6f88c0380b8993ecc651432278c67a4234624d124ff89bf6e72ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0d10ed16a5de790d6576f46c48fb64d5bb1de8959b10c7fb1c57071e528db293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402496004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e756bd965422fc177f6dd07be79fa2cb032bb3102351bb7d9a3dff27f829fe5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
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
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51871838e5ae31b0f5864921dc6d3d9f689445257df74b3f6eb5c8f8d829b9f`  
		Last Modified: Fri, 02 Feb 2024 08:55:39 GMT  
		Size: 145.3 MB (145271240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15416442087693885577f7bd84c413278afe5f2c2eb953c9b6a3c2001147ce15`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e25de628beef120796b2e0924f54e4d03ca8c5101a9b6848a9e863033ccdcad`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1ec88dbf4fb04670e9ac9b5a1fe0db140dbcd257c3aa9a0f0147e0ab2a5f1`  
		Last Modified: Fri, 02 Feb 2024 08:55:41 GMT  
		Size: 225.8 MB (225793682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c7cd5ee0d5c3ad7578a290708adcdf329707f651f136831627376ab22a743621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5348d54621325c62d7254f63118b35e3a927bce8b2f4cd873d4f996428df8e`

```dockerfile
```

-	Layers:
	-	`sha256:f39c7aa56c97e3e8df009564b4ef06b3fdb2e192f6d26869e9a957b3650db035`  
		Last Modified: Fri, 02 Feb 2024 08:55:37 GMT  
		Size: 2.6 MB (2598523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e145b75b5005d305e80188c7bdde39b8580f129e76386067d518da755b429afc`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e28c40044030a3db375b20ccc59dda967d62ff0363178bc423dd8333e07ac27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397841655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763bd13979f24e809209374281d1dcd38be2a3443a76920b4d99b826e8ea5b73`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9635450a52f740af5ea7bb2bf90de5b55f740afe251beca93580b7bc66267046`  
		Last Modified: Sat, 03 Feb 2024 08:48:14 GMT  
		Size: 142.0 MB (142006579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899a3aaa99f83e9fc9cd87849e8b16e2f96709edb28b897b123568d33de0c998`  
		Last Modified: Sat, 03 Feb 2024 08:49:13 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255e1a7b92f5ae01ed6cecfd626415ef16d78575b8ad6e65b2937797ea6125b`  
		Last Modified: Sat, 03 Feb 2024 08:49:13 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa197d29a3cd770f04dd918b207d363f47e764fd4e8be570f8b928eba495bd7`  
		Last Modified: Sat, 03 Feb 2024 08:49:20 GMT  
		Size: 225.8 MB (225757456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5682254cbe4105e4931d48fb22522ca2eafd970fcdf11b795d81c1310a481c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693c293909b843773ae7a4a203b1f15cb4165501600ca100a5c1134599a1dafb`

```dockerfile
```

-	Layers:
	-	`sha256:50b3af55b924dca48268e267a2222966e6a40c2a3e9373d4e20b941f760b398f`  
		Last Modified: Sat, 03 Feb 2024 08:49:13 GMT  
		Size: 2.6 MB (2607414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fc8c9b8626338e1b01f270de6d775c050e912ec6c80284c58338bd97418671`  
		Last Modified: Sat, 03 Feb 2024 08:49:13 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30`

```console
$ docker pull neo4j@sha256:bc346abba1c30e1ca5ec28bce8a43357adc36ab6676a37a6eeccca95a17206c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30` - linux; amd64

```console
$ docker pull neo4j@sha256:8e8117463bbf8260dcc786199c6aca82d843a3303caa770af40ac7cdbb383a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297283825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f0e5bf22f38c7ecab84732bdf0d404f8f502e0da705588a8db1e562b26fbbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
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
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ba8b81e446fea91a71d7b2fedf1f36cc5371805b772f569db46b9ec56d0e3f`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f4d805e3863a14cf676a825d60665b3b79ef71cf57e052eae3aa9a1f0ec44f`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52662ced7be079ae200c9c69496a0a723df611902c21a3d6cfe47675aae532ff`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04061e659c5d58cda64e9b84e2f9f039fd89fc80eac502c3820a9313fb3c65c5`  
		Last Modified: Fri, 02 Feb 2024 08:55:41 GMT  
		Size: 120.6 MB (120581522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30` - unknown; unknown

```console
$ docker pull neo4j@sha256:dbf81d9ad2798cad67b81903373450655381231252c5331ef7d1a09ea579d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ead4a3eadc586db63f7eff80da603796de41ce17deb75c5fc496522703826c`

```dockerfile
```

-	Layers:
	-	`sha256:ed11e124eef5338302d9ad7b3ff28eb34ee5d9a6e85f6d5fff0570dbc7e4c1a6`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 2.5 MB (2480430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae4663ab8668ba62904fb38b5ef7dfeca749e46d051234de9bc54ff785ed00e`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c70f9adf6056e4f46be400894767706878d0c77a58b3c3b7f5708d3f80987ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c903f0dfc9a6b8865426906a1d548d3f8b57948a91b3647cf6ae281b4a476dfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9635450a52f740af5ea7bb2bf90de5b55f740afe251beca93580b7bc66267046`  
		Last Modified: Sat, 03 Feb 2024 08:48:14 GMT  
		Size: 142.0 MB (142006579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377e38cfc0cbac782a756f3807641d8bd6871d2e4f6e05ec9df59e3413b81ba`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1896ba3d19a9edcd88ce13702d3e564ed4aa3d48294adc8d55d3fd0bfec225e2`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7dd7b38234441bd61821708c067ee8dd89fb525b7df24b9e9fb721820b4781`  
		Last Modified: Sat, 03 Feb 2024 08:48:13 GMT  
		Size: 120.5 MB (120547507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30` - unknown; unknown

```console
$ docker pull neo4j@sha256:22ee18af9fab1b36ea5bac688c00856119551828d46ac350ae8c2203fa6708f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2698c74ae872d7af3c48f7534f5a3314b25eb59ecd68cf1a55cfa75e4554f69`

```dockerfile
```

-	Layers:
	-	`sha256:19dc38792a3e8964b747247b734adf7d5e38304d6d087b6f8ce2f052779d05a2`  
		Last Modified: Sat, 03 Feb 2024 08:48:11 GMT  
		Size: 2.5 MB (2483929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441b336f4dd7306c3f3c7c872d24b6a10b3e266451525e681c25a38d6fc15530`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 20.2 KB (20163 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30-community`

```console
$ docker pull neo4j@sha256:bc346abba1c30e1ca5ec28bce8a43357adc36ab6676a37a6eeccca95a17206c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30-community` - linux; amd64

```console
$ docker pull neo4j@sha256:8e8117463bbf8260dcc786199c6aca82d843a3303caa770af40ac7cdbb383a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297283825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f0e5bf22f38c7ecab84732bdf0d404f8f502e0da705588a8db1e562b26fbbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
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
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ba8b81e446fea91a71d7b2fedf1f36cc5371805b772f569db46b9ec56d0e3f`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f4d805e3863a14cf676a825d60665b3b79ef71cf57e052eae3aa9a1f0ec44f`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52662ced7be079ae200c9c69496a0a723df611902c21a3d6cfe47675aae532ff`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04061e659c5d58cda64e9b84e2f9f039fd89fc80eac502c3820a9313fb3c65c5`  
		Last Modified: Fri, 02 Feb 2024 08:55:41 GMT  
		Size: 120.6 MB (120581522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:dbf81d9ad2798cad67b81903373450655381231252c5331ef7d1a09ea579d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ead4a3eadc586db63f7eff80da603796de41ce17deb75c5fc496522703826c`

```dockerfile
```

-	Layers:
	-	`sha256:ed11e124eef5338302d9ad7b3ff28eb34ee5d9a6e85f6d5fff0570dbc7e4c1a6`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 2.5 MB (2480430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae4663ab8668ba62904fb38b5ef7dfeca749e46d051234de9bc54ff785ed00e`  
		Last Modified: Fri, 02 Feb 2024 08:55:34 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c70f9adf6056e4f46be400894767706878d0c77a58b3c3b7f5708d3f80987ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c903f0dfc9a6b8865426906a1d548d3f8b57948a91b3647cf6ae281b4a476dfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9635450a52f740af5ea7bb2bf90de5b55f740afe251beca93580b7bc66267046`  
		Last Modified: Sat, 03 Feb 2024 08:48:14 GMT  
		Size: 142.0 MB (142006579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377e38cfc0cbac782a756f3807641d8bd6871d2e4f6e05ec9df59e3413b81ba`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1896ba3d19a9edcd88ce13702d3e564ed4aa3d48294adc8d55d3fd0bfec225e2`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7dd7b38234441bd61821708c067ee8dd89fb525b7df24b9e9fb721820b4781`  
		Last Modified: Sat, 03 Feb 2024 08:48:13 GMT  
		Size: 120.5 MB (120547507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:22ee18af9fab1b36ea5bac688c00856119551828d46ac350ae8c2203fa6708f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2698c74ae872d7af3c48f7534f5a3314b25eb59ecd68cf1a55cfa75e4554f69`

```dockerfile
```

-	Layers:
	-	`sha256:19dc38792a3e8964b747247b734adf7d5e38304d6d087b6f8ce2f052779d05a2`  
		Last Modified: Sat, 03 Feb 2024 08:48:11 GMT  
		Size: 2.5 MB (2483929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441b336f4dd7306c3f3c7c872d24b6a10b3e266451525e681c25a38d6fc15530`  
		Last Modified: Sat, 03 Feb 2024 08:48:10 GMT  
		Size: 20.2 KB (20163 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30-enterprise`

```console
$ docker pull neo4j@sha256:fbc9da0af3c6f88c0380b8993ecc651432278c67a4234624d124ff89bf6e72ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0d10ed16a5de790d6576f46c48fb64d5bb1de8959b10c7fb1c57071e528db293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402496004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e756bd965422fc177f6dd07be79fa2cb032bb3102351bb7d9a3dff27f829fe5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
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
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51871838e5ae31b0f5864921dc6d3d9f689445257df74b3f6eb5c8f8d829b9f`  
		Last Modified: Fri, 02 Feb 2024 08:55:39 GMT  
		Size: 145.3 MB (145271240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15416442087693885577f7bd84c413278afe5f2c2eb953c9b6a3c2001147ce15`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e25de628beef120796b2e0924f54e4d03ca8c5101a9b6848a9e863033ccdcad`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1ec88dbf4fb04670e9ac9b5a1fe0db140dbcd257c3aa9a0f0147e0ab2a5f1`  
		Last Modified: Fri, 02 Feb 2024 08:55:41 GMT  
		Size: 225.8 MB (225793682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c7cd5ee0d5c3ad7578a290708adcdf329707f651f136831627376ab22a743621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5348d54621325c62d7254f63118b35e3a927bce8b2f4cd873d4f996428df8e`

```dockerfile
```

-	Layers:
	-	`sha256:f39c7aa56c97e3e8df009564b4ef06b3fdb2e192f6d26869e9a957b3650db035`  
		Last Modified: Fri, 02 Feb 2024 08:55:37 GMT  
		Size: 2.6 MB (2598523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e145b75b5005d305e80188c7bdde39b8580f129e76386067d518da755b429afc`  
		Last Modified: Fri, 02 Feb 2024 08:55:36 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e28c40044030a3db375b20ccc59dda967d62ff0363178bc423dd8333e07ac27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397841655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763bd13979f24e809209374281d1dcd38be2a3443a76920b4d99b826e8ea5b73`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9635450a52f740af5ea7bb2bf90de5b55f740afe251beca93580b7bc66267046`  
		Last Modified: Sat, 03 Feb 2024 08:48:14 GMT  
		Size: 142.0 MB (142006579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899a3aaa99f83e9fc9cd87849e8b16e2f96709edb28b897b123568d33de0c998`  
		Last Modified: Sat, 03 Feb 2024 08:49:13 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255e1a7b92f5ae01ed6cecfd626415ef16d78575b8ad6e65b2937797ea6125b`  
		Last Modified: Sat, 03 Feb 2024 08:49:13 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa197d29a3cd770f04dd918b207d363f47e764fd4e8be570f8b928eba495bd7`  
		Last Modified: Sat, 03 Feb 2024 08:49:20 GMT  
		Size: 225.8 MB (225757456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5682254cbe4105e4931d48fb22522ca2eafd970fcdf11b795d81c1310a481c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693c293909b843773ae7a4a203b1f15cb4165501600ca100a5c1134599a1dafb`

```dockerfile
```

-	Layers:
	-	`sha256:50b3af55b924dca48268e267a2222966e6a40c2a3e9373d4e20b941f760b398f`  
		Last Modified: Sat, 03 Feb 2024 08:49:13 GMT  
		Size: 2.6 MB (2607414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fc8c9b8626338e1b01f270de6d775c050e912ec6c80284c58338bd97418671`  
		Last Modified: Sat, 03 Feb 2024 08:49:13 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:ed8f0ed168462ab3a2e22c2aefaac3d54379b0ff4cf914fd7a620d053d7e8bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1710d6cdcc87c39a6898404460836fdec33f0507ebf10b33466c46088ef0607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501d5b117210affc25e7adb689ab1528010b27d0a9e040061f69cea1dc0d53a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949494ab68acc6364427ac970911e0dd084a25be0a09010f6b30657b9f28074d`  
		Last Modified: Fri, 02 Feb 2024 08:56:00 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b15a1b69e7e0b52a766ba3d036adcae0d712ec7a7f65f96f82f04792bf5cd2`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6038b3ce145211960b33f8c931880f86320fe425e5d1241b86221f0da7c4aa7`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d99d36e63f4ef6df6a2ec693c9f6ad01142378aaefb28c812fb4f4454f31a`  
		Last Modified: Fri, 02 Feb 2024 08:56:06 GMT  
		Size: 371.4 MB (371423633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:01a9ea982056256e57e4e2c67eb768b4216759c818f636cbb56a909f22b755b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1f2a677ca7a3c127c255bebe092eb615d6f5ad9085bb4b4970804927b5e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9b90dfd6b628b7b2ebe864e28d6939ebc9bee2b3cbcae5620f3649c2bcb8de74`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242698b9ca5d1db95e986a06e05f64e925b65306c7c50907a73f75749d0da123`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c35f820a89c9b841a2195b3823ac792c898161ff364af9371913f07efe74430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545191173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ef0e290ead78940c086740ffa672e68b310b5f1ee78bea4e1c4cb04795c0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17890f1b7088b1cb173b5d9eb47e332b599ed6b964ce34ecf4af27e8d6ba6a11`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2802a199e50353ec7782f84907432dc2996a0d5e477e19b63e35b9b4b507341`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776915e068087ff82ed6e7d99aad7c7b36d7045507cf74b45ae241b40ce7489`  
		Last Modified: Sat, 03 Feb 2024 08:47:10 GMT  
		Size: 371.4 MB (371393117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:df6338d220f53a9524f3e0ac335fc155b28291a93f29a90bd0b6c22d993b8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1ea834e64bfe3735c106284a16901e63d86e95961be5d69b8d97eb6e03f61`

```dockerfile
```

-	Layers:
	-	`sha256:9a4b6888df5c544f5e81db9beb5b7b507d6a79a7dac7d1d4ed4e2e645ccaa39e`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 2.7 MB (2666014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894de020edae17026be72afff509daeacaf6eaf03dd7d50f7b1e70ae9d10bac`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:ed8f0ed168462ab3a2e22c2aefaac3d54379b0ff4cf914fd7a620d053d7e8bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1710d6cdcc87c39a6898404460836fdec33f0507ebf10b33466c46088ef0607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501d5b117210affc25e7adb689ab1528010b27d0a9e040061f69cea1dc0d53a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949494ab68acc6364427ac970911e0dd084a25be0a09010f6b30657b9f28074d`  
		Last Modified: Fri, 02 Feb 2024 08:56:00 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b15a1b69e7e0b52a766ba3d036adcae0d712ec7a7f65f96f82f04792bf5cd2`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6038b3ce145211960b33f8c931880f86320fe425e5d1241b86221f0da7c4aa7`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d99d36e63f4ef6df6a2ec693c9f6ad01142378aaefb28c812fb4f4454f31a`  
		Last Modified: Fri, 02 Feb 2024 08:56:06 GMT  
		Size: 371.4 MB (371423633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:01a9ea982056256e57e4e2c67eb768b4216759c818f636cbb56a909f22b755b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1f2a677ca7a3c127c255bebe092eb615d6f5ad9085bb4b4970804927b5e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9b90dfd6b628b7b2ebe864e28d6939ebc9bee2b3cbcae5620f3649c2bcb8de74`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242698b9ca5d1db95e986a06e05f64e925b65306c7c50907a73f75749d0da123`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c35f820a89c9b841a2195b3823ac792c898161ff364af9371913f07efe74430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545191173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ef0e290ead78940c086740ffa672e68b310b5f1ee78bea4e1c4cb04795c0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17890f1b7088b1cb173b5d9eb47e332b599ed6b964ce34ecf4af27e8d6ba6a11`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2802a199e50353ec7782f84907432dc2996a0d5e477e19b63e35b9b4b507341`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776915e068087ff82ed6e7d99aad7c7b36d7045507cf74b45ae241b40ce7489`  
		Last Modified: Sat, 03 Feb 2024 08:47:10 GMT  
		Size: 371.4 MB (371393117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:df6338d220f53a9524f3e0ac335fc155b28291a93f29a90bd0b6c22d993b8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1ea834e64bfe3735c106284a16901e63d86e95961be5d69b8d97eb6e03f61`

```dockerfile
```

-	Layers:
	-	`sha256:9a4b6888df5c544f5e81db9beb5b7b507d6a79a7dac7d1d4ed4e2e645ccaa39e`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 2.7 MB (2666014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894de020edae17026be72afff509daeacaf6eaf03dd7d50f7b1e70ae9d10bac`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:9f51a5f6a8bcb6fdd62ab508afdd1d834fc7831485de9df2a79532d9299e1554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7a9eabe22e802af5761350a4762280848cbbb7ca6819392aaec11ac5936ebd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559974948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b29c77001dafe383df7e5bbc3f0da069b210432c791be470b8b9e7971ec5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428ce3e4156088dba5f9a936aa203bf0209e3dc078d3e7471f2ff554b3f2de1`  
		Last Modified: Mon, 05 Feb 2024 21:52:00 GMT  
		Size: 152.2 MB (152177043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f439e7a8d82c07a57f8f51fc698aa9a3479784e5dd62b6a894d09711d7ea1a6`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced9340d9865370122c1b9953a8d65277c8fba4d6b392be64a702070f8ee33d`  
		Last Modified: Mon, 05 Feb 2024 21:52:04 GMT  
		Size: 368.5 MB (368496317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:21ac93bd2ba8887bea839f0d54d347c0ff4416ef4e44a73577118b2d91e47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9023828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863073c6981bbb2ee3493a34843562517505f54dffc000667bd8c1f031a45722`

```dockerfile
```

-	Layers:
	-	`sha256:31a38617eaeaaa5bed9990e291d8a01fedfc7de8c86e7e39ab2c80005ed68fd3`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.0 MB (9003592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d2101f1fa58d0e564da48e808e2f031c6eb05ff8ed8edb6ab34094b7eec170`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-bullseye`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community-bullseye`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise`

```console
$ docker pull neo4j@sha256:ed8f0ed168462ab3a2e22c2aefaac3d54379b0ff4cf914fd7a620d053d7e8bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1710d6cdcc87c39a6898404460836fdec33f0507ebf10b33466c46088ef0607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501d5b117210affc25e7adb689ab1528010b27d0a9e040061f69cea1dc0d53a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949494ab68acc6364427ac970911e0dd084a25be0a09010f6b30657b9f28074d`  
		Last Modified: Fri, 02 Feb 2024 08:56:00 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b15a1b69e7e0b52a766ba3d036adcae0d712ec7a7f65f96f82f04792bf5cd2`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6038b3ce145211960b33f8c931880f86320fe425e5d1241b86221f0da7c4aa7`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d99d36e63f4ef6df6a2ec693c9f6ad01142378aaefb28c812fb4f4454f31a`  
		Last Modified: Fri, 02 Feb 2024 08:56:06 GMT  
		Size: 371.4 MB (371423633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:01a9ea982056256e57e4e2c67eb768b4216759c818f636cbb56a909f22b755b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1f2a677ca7a3c127c255bebe092eb615d6f5ad9085bb4b4970804927b5e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9b90dfd6b628b7b2ebe864e28d6939ebc9bee2b3cbcae5620f3649c2bcb8de74`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242698b9ca5d1db95e986a06e05f64e925b65306c7c50907a73f75749d0da123`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c35f820a89c9b841a2195b3823ac792c898161ff364af9371913f07efe74430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545191173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ef0e290ead78940c086740ffa672e68b310b5f1ee78bea4e1c4cb04795c0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17890f1b7088b1cb173b5d9eb47e332b599ed6b964ce34ecf4af27e8d6ba6a11`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2802a199e50353ec7782f84907432dc2996a0d5e477e19b63e35b9b4b507341`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776915e068087ff82ed6e7d99aad7c7b36d7045507cf74b45ae241b40ce7489`  
		Last Modified: Sat, 03 Feb 2024 08:47:10 GMT  
		Size: 371.4 MB (371393117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:df6338d220f53a9524f3e0ac335fc155b28291a93f29a90bd0b6c22d993b8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1ea834e64bfe3735c106284a16901e63d86e95961be5d69b8d97eb6e03f61`

```dockerfile
```

-	Layers:
	-	`sha256:9a4b6888df5c544f5e81db9beb5b7b507d6a79a7dac7d1d4ed4e2e645ccaa39e`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 2.7 MB (2666014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894de020edae17026be72afff509daeacaf6eaf03dd7d50f7b1e70ae9d10bac`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:ed8f0ed168462ab3a2e22c2aefaac3d54379b0ff4cf914fd7a620d053d7e8bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1710d6cdcc87c39a6898404460836fdec33f0507ebf10b33466c46088ef0607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501d5b117210affc25e7adb689ab1528010b27d0a9e040061f69cea1dc0d53a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949494ab68acc6364427ac970911e0dd084a25be0a09010f6b30657b9f28074d`  
		Last Modified: Fri, 02 Feb 2024 08:56:00 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b15a1b69e7e0b52a766ba3d036adcae0d712ec7a7f65f96f82f04792bf5cd2`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6038b3ce145211960b33f8c931880f86320fe425e5d1241b86221f0da7c4aa7`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d99d36e63f4ef6df6a2ec693c9f6ad01142378aaefb28c812fb4f4454f31a`  
		Last Modified: Fri, 02 Feb 2024 08:56:06 GMT  
		Size: 371.4 MB (371423633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:01a9ea982056256e57e4e2c67eb768b4216759c818f636cbb56a909f22b755b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1f2a677ca7a3c127c255bebe092eb615d6f5ad9085bb4b4970804927b5e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9b90dfd6b628b7b2ebe864e28d6939ebc9bee2b3cbcae5620f3649c2bcb8de74`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242698b9ca5d1db95e986a06e05f64e925b65306c7c50907a73f75749d0da123`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c35f820a89c9b841a2195b3823ac792c898161ff364af9371913f07efe74430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545191173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ef0e290ead78940c086740ffa672e68b310b5f1ee78bea4e1c4cb04795c0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17890f1b7088b1cb173b5d9eb47e332b599ed6b964ce34ecf4af27e8d6ba6a11`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2802a199e50353ec7782f84907432dc2996a0d5e477e19b63e35b9b4b507341`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776915e068087ff82ed6e7d99aad7c7b36d7045507cf74b45ae241b40ce7489`  
		Last Modified: Sat, 03 Feb 2024 08:47:10 GMT  
		Size: 371.4 MB (371393117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:df6338d220f53a9524f3e0ac335fc155b28291a93f29a90bd0b6c22d993b8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1ea834e64bfe3735c106284a16901e63d86e95961be5d69b8d97eb6e03f61`

```dockerfile
```

-	Layers:
	-	`sha256:9a4b6888df5c544f5e81db9beb5b7b507d6a79a7dac7d1d4ed4e2e645ccaa39e`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 2.7 MB (2666014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894de020edae17026be72afff509daeacaf6eaf03dd7d50f7b1e70ae9d10bac`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:9f51a5f6a8bcb6fdd62ab508afdd1d834fc7831485de9df2a79532d9299e1554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7a9eabe22e802af5761350a4762280848cbbb7ca6819392aaec11ac5936ebd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559974948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b29c77001dafe383df7e5bbc3f0da069b210432c791be470b8b9e7971ec5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428ce3e4156088dba5f9a936aa203bf0209e3dc078d3e7471f2ff554b3f2de1`  
		Last Modified: Mon, 05 Feb 2024 21:52:00 GMT  
		Size: 152.2 MB (152177043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f439e7a8d82c07a57f8f51fc698aa9a3479784e5dd62b6a894d09711d7ea1a6`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced9340d9865370122c1b9953a8d65277c8fba4d6b392be64a702070f8ee33d`  
		Last Modified: Mon, 05 Feb 2024 21:52:04 GMT  
		Size: 368.5 MB (368496317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:21ac93bd2ba8887bea839f0d54d347c0ff4416ef4e44a73577118b2d91e47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9023828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863073c6981bbb2ee3493a34843562517505f54dffc000667bd8c1f031a45722`

```dockerfile
```

-	Layers:
	-	`sha256:31a38617eaeaaa5bed9990e291d8a01fedfc7de8c86e7e39ab2c80005ed68fd3`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.0 MB (9003592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d2101f1fa58d0e564da48e808e2f031c6eb05ff8ed8edb6ab34094b7eec170`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-bullseye`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community-bullseye`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise`

```console
$ docker pull neo4j@sha256:ed8f0ed168462ab3a2e22c2aefaac3d54379b0ff4cf914fd7a620d053d7e8bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1710d6cdcc87c39a6898404460836fdec33f0507ebf10b33466c46088ef0607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501d5b117210affc25e7adb689ab1528010b27d0a9e040061f69cea1dc0d53a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949494ab68acc6364427ac970911e0dd084a25be0a09010f6b30657b9f28074d`  
		Last Modified: Fri, 02 Feb 2024 08:56:00 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b15a1b69e7e0b52a766ba3d036adcae0d712ec7a7f65f96f82f04792bf5cd2`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6038b3ce145211960b33f8c931880f86320fe425e5d1241b86221f0da7c4aa7`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d99d36e63f4ef6df6a2ec693c9f6ad01142378aaefb28c812fb4f4454f31a`  
		Last Modified: Fri, 02 Feb 2024 08:56:06 GMT  
		Size: 371.4 MB (371423633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:01a9ea982056256e57e4e2c67eb768b4216759c818f636cbb56a909f22b755b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1f2a677ca7a3c127c255bebe092eb615d6f5ad9085bb4b4970804927b5e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9b90dfd6b628b7b2ebe864e28d6939ebc9bee2b3cbcae5620f3649c2bcb8de74`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242698b9ca5d1db95e986a06e05f64e925b65306c7c50907a73f75749d0da123`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c35f820a89c9b841a2195b3823ac792c898161ff364af9371913f07efe74430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545191173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ef0e290ead78940c086740ffa672e68b310b5f1ee78bea4e1c4cb04795c0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17890f1b7088b1cb173b5d9eb47e332b599ed6b964ce34ecf4af27e8d6ba6a11`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2802a199e50353ec7782f84907432dc2996a0d5e477e19b63e35b9b4b507341`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776915e068087ff82ed6e7d99aad7c7b36d7045507cf74b45ae241b40ce7489`  
		Last Modified: Sat, 03 Feb 2024 08:47:10 GMT  
		Size: 371.4 MB (371393117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:df6338d220f53a9524f3e0ac335fc155b28291a93f29a90bd0b6c22d993b8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1ea834e64bfe3735c106284a16901e63d86e95961be5d69b8d97eb6e03f61`

```dockerfile
```

-	Layers:
	-	`sha256:9a4b6888df5c544f5e81db9beb5b7b507d6a79a7dac7d1d4ed4e2e645ccaa39e`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 2.7 MB (2666014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894de020edae17026be72afff509daeacaf6eaf03dd7d50f7b1e70ae9d10bac`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:ed8f0ed168462ab3a2e22c2aefaac3d54379b0ff4cf914fd7a620d053d7e8bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1710d6cdcc87c39a6898404460836fdec33f0507ebf10b33466c46088ef0607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501d5b117210affc25e7adb689ab1528010b27d0a9e040061f69cea1dc0d53a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949494ab68acc6364427ac970911e0dd084a25be0a09010f6b30657b9f28074d`  
		Last Modified: Fri, 02 Feb 2024 08:56:00 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b15a1b69e7e0b52a766ba3d036adcae0d712ec7a7f65f96f82f04792bf5cd2`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6038b3ce145211960b33f8c931880f86320fe425e5d1241b86221f0da7c4aa7`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d99d36e63f4ef6df6a2ec693c9f6ad01142378aaefb28c812fb4f4454f31a`  
		Last Modified: Fri, 02 Feb 2024 08:56:06 GMT  
		Size: 371.4 MB (371423633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:01a9ea982056256e57e4e2c67eb768b4216759c818f636cbb56a909f22b755b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1f2a677ca7a3c127c255bebe092eb615d6f5ad9085bb4b4970804927b5e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9b90dfd6b628b7b2ebe864e28d6939ebc9bee2b3cbcae5620f3649c2bcb8de74`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242698b9ca5d1db95e986a06e05f64e925b65306c7c50907a73f75749d0da123`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c35f820a89c9b841a2195b3823ac792c898161ff364af9371913f07efe74430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545191173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ef0e290ead78940c086740ffa672e68b310b5f1ee78bea4e1c4cb04795c0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17890f1b7088b1cb173b5d9eb47e332b599ed6b964ce34ecf4af27e8d6ba6a11`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2802a199e50353ec7782f84907432dc2996a0d5e477e19b63e35b9b4b507341`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776915e068087ff82ed6e7d99aad7c7b36d7045507cf74b45ae241b40ce7489`  
		Last Modified: Sat, 03 Feb 2024 08:47:10 GMT  
		Size: 371.4 MB (371393117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:df6338d220f53a9524f3e0ac335fc155b28291a93f29a90bd0b6c22d993b8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1ea834e64bfe3735c106284a16901e63d86e95961be5d69b8d97eb6e03f61`

```dockerfile
```

-	Layers:
	-	`sha256:9a4b6888df5c544f5e81db9beb5b7b507d6a79a7dac7d1d4ed4e2e645ccaa39e`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 2.7 MB (2666014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894de020edae17026be72afff509daeacaf6eaf03dd7d50f7b1e70ae9d10bac`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:9f51a5f6a8bcb6fdd62ab508afdd1d834fc7831485de9df2a79532d9299e1554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7a9eabe22e802af5761350a4762280848cbbb7ca6819392aaec11ac5936ebd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559974948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b29c77001dafe383df7e5bbc3f0da069b210432c791be470b8b9e7971ec5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428ce3e4156088dba5f9a936aa203bf0209e3dc078d3e7471f2ff554b3f2de1`  
		Last Modified: Mon, 05 Feb 2024 21:52:00 GMT  
		Size: 152.2 MB (152177043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f439e7a8d82c07a57f8f51fc698aa9a3479784e5dd62b6a894d09711d7ea1a6`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced9340d9865370122c1b9953a8d65277c8fba4d6b392be64a702070f8ee33d`  
		Last Modified: Mon, 05 Feb 2024 21:52:04 GMT  
		Size: 368.5 MB (368496317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:21ac93bd2ba8887bea839f0d54d347c0ff4416ef4e44a73577118b2d91e47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9023828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863073c6981bbb2ee3493a34843562517505f54dffc000667bd8c1f031a45722`

```dockerfile
```

-	Layers:
	-	`sha256:31a38617eaeaaa5bed9990e291d8a01fedfc7de8c86e7e39ab2c80005ed68fd3`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.0 MB (9003592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d2101f1fa58d0e564da48e808e2f031c6eb05ff8ed8edb6ab34094b7eec170`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:ed8f0ed168462ab3a2e22c2aefaac3d54379b0ff4cf914fd7a620d053d7e8bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1710d6cdcc87c39a6898404460836fdec33f0507ebf10b33466c46088ef0607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501d5b117210affc25e7adb689ab1528010b27d0a9e040061f69cea1dc0d53a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949494ab68acc6364427ac970911e0dd084a25be0a09010f6b30657b9f28074d`  
		Last Modified: Fri, 02 Feb 2024 08:56:00 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b15a1b69e7e0b52a766ba3d036adcae0d712ec7a7f65f96f82f04792bf5cd2`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6038b3ce145211960b33f8c931880f86320fe425e5d1241b86221f0da7c4aa7`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d99d36e63f4ef6df6a2ec693c9f6ad01142378aaefb28c812fb4f4454f31a`  
		Last Modified: Fri, 02 Feb 2024 08:56:06 GMT  
		Size: 371.4 MB (371423633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:01a9ea982056256e57e4e2c67eb768b4216759c818f636cbb56a909f22b755b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1f2a677ca7a3c127c255bebe092eb615d6f5ad9085bb4b4970804927b5e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9b90dfd6b628b7b2ebe864e28d6939ebc9bee2b3cbcae5620f3649c2bcb8de74`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242698b9ca5d1db95e986a06e05f64e925b65306c7c50907a73f75749d0da123`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c35f820a89c9b841a2195b3823ac792c898161ff364af9371913f07efe74430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545191173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ef0e290ead78940c086740ffa672e68b310b5f1ee78bea4e1c4cb04795c0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17890f1b7088b1cb173b5d9eb47e332b599ed6b964ce34ecf4af27e8d6ba6a11`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2802a199e50353ec7782f84907432dc2996a0d5e477e19b63e35b9b4b507341`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776915e068087ff82ed6e7d99aad7c7b36d7045507cf74b45ae241b40ce7489`  
		Last Modified: Sat, 03 Feb 2024 08:47:10 GMT  
		Size: 371.4 MB (371393117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:df6338d220f53a9524f3e0ac335fc155b28291a93f29a90bd0b6c22d993b8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1ea834e64bfe3735c106284a16901e63d86e95961be5d69b8d97eb6e03f61`

```dockerfile
```

-	Layers:
	-	`sha256:9a4b6888df5c544f5e81db9beb5b7b507d6a79a7dac7d1d4ed4e2e645ccaa39e`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 2.7 MB (2666014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894de020edae17026be72afff509daeacaf6eaf03dd7d50f7b1e70ae9d10bac`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:ed8f0ed168462ab3a2e22c2aefaac3d54379b0ff4cf914fd7a620d053d7e8bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1710d6cdcc87c39a6898404460836fdec33f0507ebf10b33466c46088ef0607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501d5b117210affc25e7adb689ab1528010b27d0a9e040061f69cea1dc0d53a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949494ab68acc6364427ac970911e0dd084a25be0a09010f6b30657b9f28074d`  
		Last Modified: Fri, 02 Feb 2024 08:56:00 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b15a1b69e7e0b52a766ba3d036adcae0d712ec7a7f65f96f82f04792bf5cd2`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6038b3ce145211960b33f8c931880f86320fe425e5d1241b86221f0da7c4aa7`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d99d36e63f4ef6df6a2ec693c9f6ad01142378aaefb28c812fb4f4454f31a`  
		Last Modified: Fri, 02 Feb 2024 08:56:06 GMT  
		Size: 371.4 MB (371423633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:01a9ea982056256e57e4e2c67eb768b4216759c818f636cbb56a909f22b755b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1f2a677ca7a3c127c255bebe092eb615d6f5ad9085bb4b4970804927b5e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9b90dfd6b628b7b2ebe864e28d6939ebc9bee2b3cbcae5620f3649c2bcb8de74`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242698b9ca5d1db95e986a06e05f64e925b65306c7c50907a73f75749d0da123`  
		Last Modified: Fri, 02 Feb 2024 08:55:56 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c35f820a89c9b841a2195b3823ac792c898161ff364af9371913f07efe74430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545191173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ef0e290ead78940c086740ffa672e68b310b5f1ee78bea4e1c4cb04795c0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17890f1b7088b1cb173b5d9eb47e332b599ed6b964ce34ecf4af27e8d6ba6a11`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2802a199e50353ec7782f84907432dc2996a0d5e477e19b63e35b9b4b507341`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776915e068087ff82ed6e7d99aad7c7b36d7045507cf74b45ae241b40ce7489`  
		Last Modified: Sat, 03 Feb 2024 08:47:10 GMT  
		Size: 371.4 MB (371393117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:df6338d220f53a9524f3e0ac335fc155b28291a93f29a90bd0b6c22d993b8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1ea834e64bfe3735c106284a16901e63d86e95961be5d69b8d97eb6e03f61`

```dockerfile
```

-	Layers:
	-	`sha256:9a4b6888df5c544f5e81db9beb5b7b507d6a79a7dac7d1d4ed4e2e645ccaa39e`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 2.7 MB (2666014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894de020edae17026be72afff509daeacaf6eaf03dd7d50f7b1e70ae9d10bac`  
		Last Modified: Sat, 03 Feb 2024 08:47:02 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:9f51a5f6a8bcb6fdd62ab508afdd1d834fc7831485de9df2a79532d9299e1554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7a9eabe22e802af5761350a4762280848cbbb7ca6819392aaec11ac5936ebd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559974948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b29c77001dafe383df7e5bbc3f0da069b210432c791be470b8b9e7971ec5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428ce3e4156088dba5f9a936aa203bf0209e3dc078d3e7471f2ff554b3f2de1`  
		Last Modified: Mon, 05 Feb 2024 21:52:00 GMT  
		Size: 152.2 MB (152177043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f439e7a8d82c07a57f8f51fc698aa9a3479784e5dd62b6a894d09711d7ea1a6`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced9340d9865370122c1b9953a8d65277c8fba4d6b392be64a702070f8ee33d`  
		Last Modified: Mon, 05 Feb 2024 21:52:04 GMT  
		Size: 368.5 MB (368496317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:21ac93bd2ba8887bea839f0d54d347c0ff4416ef4e44a73577118b2d91e47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9023828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863073c6981bbb2ee3493a34843562517505f54dffc000667bd8c1f031a45722`

```dockerfile
```

-	Layers:
	-	`sha256:31a38617eaeaaa5bed9990e291d8a01fedfc7de8c86e7e39ab2c80005ed68fd3`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.0 MB (9003592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d2101f1fa58d0e564da48e808e2f031c6eb05ff8ed8edb6ab34094b7eec170`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:ac583ef49bbf209895d2ec54b16d39fe52b5f7db5790e6fb1bea1f52c0b10452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:a27c2257dc33975164e0d57f40bced44981a0d61919c831eeb16173157f1a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6f672547ca2ab6b02f26dd3ae84f8488503576527beca67d7e1486d72c6ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828b8e7cb79ed5eddfec325e4ae784c5556bb0fcb7422a0c8d60c874f77bd176`  
		Last Modified: Fri, 02 Feb 2024 08:55:25 GMT  
		Size: 144.9 MB (144893015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72572e3a6b2d2389f562036319d43b7679effbf257ebeb2f31d7aa168b500e76`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3115b8c9b13605f9a24a31228c9a1c204310d09f0919f10cac86e3c3d6acb8b`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f47895acc71325741d0dcf60f9898a6312dc79df7133fd2d5106dc3cfedff0`  
		Last Modified: Fri, 02 Feb 2024 08:55:24 GMT  
		Size: 115.4 MB (115406114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:0855a14c2645cd2faa31e8be381690ce6a8fe33130b29c67f703140be36b6ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44830e06b9ddaac39a7010147fb2cb443a53c66d0f88514693e80d997494df70`

```dockerfile
```

-	Layers:
	-	`sha256:0eb045a61216dcd30b5f3368f6dcf603f1521c140a630e6415668691cf15051d`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fd9714e9d958b0fd09ec06628b440fbdb3136923a9283dca965ce2dc58e788`  
		Last Modified: Fri, 02 Feb 2024 08:55:22 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:864f88df1ee84fdfa821a84ec6cbe5f310f55aca287260716afad89a3b2ea7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02426a341cda1be4b183947b171775f2c33ac3033f7768a471619ed2ced988`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157cba4c2a4a126c1c6da79051e54a19ff4fb96a95f967df72f13355fa18409e`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 143.7 MB (143720366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd3704dc234a377c6a73e095f359889454f8c5eb32e6921f6bc17d8de94f90`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c15f94ce1631c09c99705263585db778cf9360d01660e0ff24fdd71031592`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb090e17c2bb4896d374578623d29c060974b143f2727140dcbedce3670b70a`  
		Last Modified: Sat, 03 Feb 2024 08:45:52 GMT  
		Size: 115.4 MB (115369109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:e961cc99a64c3b49c74702350a0c7b839adc75a7f489b760d0606771b9e56402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9559173ae67e540fb4bc75dccd60e02b4973982943faeee340a18f0be02280a1`

```dockerfile
```

-	Layers:
	-	`sha256:30604aef4a7fb034ec65fc0daf52dbd57ed2bf5595f83c0e20a57b056ef7772c`  
		Last Modified: Sat, 03 Feb 2024 08:45:49 GMT  
		Size: 2.5 MB (2474503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62aa0e380e98b714399ad4fb5ace6947720891a006bb7a1b0fe0368af41914`  
		Last Modified: Sat, 03 Feb 2024 08:45:48 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json
