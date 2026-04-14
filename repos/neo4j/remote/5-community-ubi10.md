## `neo4j:5-community-ubi10`

```console
$ docker pull neo4j@sha256:810331f06505d11afaefb30b28d29fce5f1904905e5c2e23b03bac7c9c0265d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:79e5ca6fc5b715f58c935cf921462e481f7330ab9b1cf428463edf2398b7fe7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287394304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572e84ca8b41e2df5e7f17d70015ec9fa0769724d0c669d79ae23b36a03cf05a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:14:03 GMT
ENV container oci
# Mon, 13 Apr 2026 09:14:04 GMT
COPY dir:76b09a495622d7b6331e3b1ce0727af742be820fe3eaf865e896be5c160bcdbe in /      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:14:04 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:95047be8e40b1e3c668ac62dda8bcb33d863723da6a80c1b3ce4f34f04292a93 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:95047be8e40b1e3c668ac62dda8bcb33d863723da6a80c1b3ce4f34f04292a93 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:14:05 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:13:50Z" "org.opencontainers.image.created"="2026-04-13T09:13:50Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:13:50Z
# Tue, 14 Apr 2026 00:00:32 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:00:32 GMT
ENV NEO4J_SHA256=9e17d344f00a50a5befb8ef8eb29f08bb56945e5334562c05457a03651657c85 NEO4J_TARBALL=neo4j-community-5.26.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 14 Apr 2026 00:00:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
# Tue, 14 Apr 2026 00:00:32 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 Apr 2026 00:00:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 14 Apr 2026 00:00:41 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:00:41 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 Apr 2026 00:00:41 GMT
VOLUME [/data /logs]
# Tue, 14 Apr 2026 00:00:41 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 Apr 2026 00:00:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 00:00:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f0c6a9d8564d2a3d188b4b49db41fad56fb7e4756edf376c0ff881d93ab0da5e`  
		Last Modified: Mon, 13 Apr 2026 10:09:42 GMT  
		Size: 34.6 MB (34605867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7753086b20c8e9d099d8a93f81ccefbd0c5f44d23e29372acd684ccc28517bde`  
		Last Modified: Tue, 14 Apr 2026 00:01:01 GMT  
		Size: 85.9 MB (85871811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162219e03bb24ff59e0e3755bc37d4446e401a8ecdc3d9eb8595136d90ed70d2`  
		Last Modified: Tue, 14 Apr 2026 00:00:58 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad0985afc34e61158b2f32d9b114986726198e3b7296d5a6adda119c5a7977e`  
		Last Modified: Tue, 14 Apr 2026 00:01:03 GMT  
		Size: 166.9 MB (166906532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:6694a8c46aa2737aa7b8132edb54514373f157f8bafe2afd977dee6aea54e196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1632483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a42e1c97b8089211d51a0312a7395257373a4134663b7e170f2bc6c9613cac`

```dockerfile
```

-	Layers:
	-	`sha256:61efbf7c6ac5b9565f95ba37a6098b07c521ecba5393a675ccaaacbcd5a555f9`  
		Last Modified: Tue, 14 Apr 2026 00:00:58 GMT  
		Size: 1.6 MB (1611536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe82f63f847c6310ec583278859533315a3a9a681490ea0665c0ecd8ceb1c49`  
		Last Modified: Tue, 14 Apr 2026 00:00:58 GMT  
		Size: 20.9 KB (20947 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3927638f1b34f06a559f9316cc3b4a9982c98d94241e882d39e77fd306be6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284401685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6307898231c856913308ca9f42660ef8ca4eb02b71de09d20d6f6cb0ce4793a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:16:58 GMT
ENV container oci
# Mon, 13 Apr 2026 09:16:58 GMT
COPY dir:e4f84a8805207b4cd31715d3ea15f1b5641e6568c620ec6afade1b03163f2ec3 in /      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:16:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:d8a3d61eb5d229916123ad1cb0753c18ec7103c4e50b2eea20333708695dac3e in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:d8a3d61eb5d229916123ad1cb0753c18ec7103c4e50b2eea20333708695dac3e in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:16:59 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:16:42Z" "org.opencontainers.image.created"="2026-04-13T09:16:42Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:16:42Z
# Tue, 14 Apr 2026 00:01:21 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:01:21 GMT
ENV NEO4J_SHA256=9e17d344f00a50a5befb8ef8eb29f08bb56945e5334562c05457a03651657c85 NEO4J_TARBALL=neo4j-community-5.26.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 14 Apr 2026 00:01:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
# Tue, 14 Apr 2026 00:01:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 Apr 2026 00:01:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 14 Apr 2026 00:01:24 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 Apr 2026 00:01:24 GMT
VOLUME [/data /logs]
# Tue, 14 Apr 2026 00:01:24 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 Apr 2026 00:01:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 00:01:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:412494b6387e552210df602617d718496fdcb1172b467aad0caa041e910fd015`  
		Last Modified: Mon, 13 Apr 2026 11:58:02 GMT  
		Size: 32.7 MB (32680047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b860503a254087d55916ac94740de8addab972b3fb70cfb9b5aacf9c65371`  
		Last Modified: Tue, 14 Apr 2026 00:01:46 GMT  
		Size: 84.8 MB (84805005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5615daada800b9c234ef55b9830c8447f395e47ae4f1860c321798ea19460f71`  
		Last Modified: Tue, 14 Apr 2026 00:01:42 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13c43706847578b6500e1342d29107132e2da064335ed5868fc33d9f6ce5b64`  
		Last Modified: Tue, 14 Apr 2026 00:01:48 GMT  
		Size: 166.9 MB (166906539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:61837e615c4ee3a4a5b5364d3ce1848997e9112d48e020cf44d2c2760325731d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1631905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4a8cd71d4ed2966057a6b38e0b44d25ea6013365aebf92f56ae43a4d026346`

```dockerfile
```

-	Layers:
	-	`sha256:c89ef914614b6d1f2cb939569a0ff8bfde8e4a47c6e5ee7a2be0b3c759dead45`  
		Last Modified: Tue, 14 Apr 2026 00:01:42 GMT  
		Size: 1.6 MB (1610819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc054d1093a674b6a0823e6e0008bfdfcaabae920b24a0bb8f1880b7a8efaa6b`  
		Last Modified: Tue, 14 Apr 2026 00:01:41 GMT  
		Size: 21.1 KB (21086 bytes)  
		MIME: application/vnd.in-toto+json
