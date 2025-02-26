## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:4ed5c7f9a5f2fc403b2f46f7f569f622f09b6fb0512c88b2308572fbe5e361d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:49725d5b5c2ca9c16912219b602d04fd85e2f902d8e6ea8ddd806169c3b442d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333518095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03b33a7a41ecb7d5945c2b159793964b36b61e766df91d2d26fae8eeec767f5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Feb 2025 04:20:08 GMT
ENV container oci
# Thu, 13 Feb 2025 04:20:08 GMT
COPY dir:0423d0cd4a34047821e55a2806cb02fc682f017fba03e4344223878a61041986 in / 
# Thu, 13 Feb 2025 04:20:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Feb 2025 04:20:08 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 04:20:08 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL "build-date"="2025-02-13T04:19:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 13 Feb 2025 04:20:12 GMT
RUN /bin/sh
# Mon, 24 Feb 2025 12:12:23 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
ENV NEO4J_SHA256=1e0b527f0c134869020d3fb1b7af7fa69d93d429117c500f7acce953ee7c7d7f NEO4J_TARBALL=neo4j-community-5.26.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 24 Feb 2025 12:12:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.3-unix.tar.gz
# Mon, 24 Feb 2025 12:12:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Feb 2025 12:12:23 GMT
WORKDIR /var/lib/neo4j
# Mon, 24 Feb 2025 12:12:23 GMT
VOLUME [/data /logs]
# Mon, 24 Feb 2025 12:12:23 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 24 Feb 2025 12:12:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 24 Feb 2025 12:12:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3333307dcd2e4279579646a05a5f99082a61a20906175240445b0e15f73b6d6e`  
		Last Modified: Thu, 13 Feb 2025 05:39:37 GMT  
		Size: 39.4 MB (39366553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025173ec0b35686a33458b367c2a6e898c824f57a07925c25d26a0cfb5f2e50`  
		Last Modified: Thu, 13 Feb 2025 05:39:36 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a009dea9cc6f2f02e7748de5e58a7ac9b474dc9f1c78b7317d869c795b8cb32`  
		Last Modified: Tue, 25 Feb 2025 18:30:18 GMT  
		Size: 133.8 MB (133841945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d51ab2b9dd37e10aff0bbb0aaf9287a8bfd74205b955f0d2c984950bcd071e2`  
		Last Modified: Tue, 25 Feb 2025 18:30:14 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c163cf27176745c8c16262c0df8e5d36a5df693e4adbfd5bbb15ba5a3bb86c`  
		Last Modified: Tue, 25 Feb 2025 18:30:18 GMT  
		Size: 160.3 MB (160299071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6e422d5d4b6f47e523c3095fc46007a8a3f27b9987897b2b13b402a41b09a65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6401736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657dca9a83ffac48bdfc954fb0aff8863255bcf5142161f7d6e478999d52306a`

```dockerfile
```

-	Layers:
	-	`sha256:7985b97a0c3b7009e048080cdd478e3b21bdb7f3e17688713b97f77ccb875f1e`  
		Last Modified: Tue, 25 Feb 2025 18:30:14 GMT  
		Size: 6.4 MB (6379803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb4af04b8e6eafc78b4741cbc488e9dd0d9ec70e8cd459a228e75e9ac2cfc47`  
		Last Modified: Tue, 25 Feb 2025 18:30:14 GMT  
		Size: 21.9 KB (21933 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d53863b5d554a544a83279b0f46964cb57986df6ac5af65408a2f0342f1bfbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331785888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f60c04c8acf5a9b1ac29c1697983d4e7bd5de775a5ffc53f14072b3189238ae`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Feb 2025 04:25:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Feb 2025 04:25:41 GMT
ENV container oci
# Thu, 13 Feb 2025 04:25:42 GMT
COPY dir:5809c16e2c5c048de6a8d8eea9437ac183b7d2503e26b24a2422ead5736aecad in / 
# Thu, 13 Feb 2025 04:25:42 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Feb 2025 04:25:42 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 04:25:43 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Feb 2025 04:25:43 GMT
LABEL "build-date"="2025-02-13T04:25:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 13 Feb 2025 04:25:54 GMT
RUN /bin/sh
# Mon, 24 Feb 2025 12:12:23 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
ENV NEO4J_SHA256=1e0b527f0c134869020d3fb1b7af7fa69d93d429117c500f7acce953ee7c7d7f NEO4J_TARBALL=neo4j-community-5.26.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 24 Feb 2025 12:12:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.3-unix.tar.gz
# Mon, 24 Feb 2025 12:12:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Feb 2025 12:12:23 GMT
WORKDIR /var/lib/neo4j
# Mon, 24 Feb 2025 12:12:23 GMT
VOLUME [/data /logs]
# Mon, 24 Feb 2025 12:12:23 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 24 Feb 2025 12:12:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 24 Feb 2025 12:12:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:56631da24b0de345717238daea2e3e61c768d081572916ae06b08b19126a740d`  
		Last Modified: Thu, 13 Feb 2025 06:13:12 GMT  
		Size: 37.6 MB (37626059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aee836c3728069e82153bf7b209c409d3343adaea6ab6b31546e5ce09250db5`  
		Last Modified: Thu, 13 Feb 2025 06:13:10 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e9dcb3fddcec26d69184280e60463832dc318dd3d7a65170ceb3ad486c8f0c`  
		Last Modified: Fri, 14 Feb 2025 01:21:40 GMT  
		Size: 133.9 MB (133850200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46c8d92ce03f18ef5f8e436067f3265c6f648ad94d2ae88348d9d3a690ae2e1`  
		Last Modified: Fri, 14 Feb 2025 01:21:37 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c364875bb6c3ba74f2f085d97e479c42f5ea3e14ed43470f7fcf6d071692740`  
		Last Modified: Tue, 25 Feb 2025 23:58:53 GMT  
		Size: 160.3 MB (160299106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:201d332b30a0450dab9ded2198ac2196064ebbed25c342587068d1f354a8cd6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32a436b9051debe5c456b24ecb0c747ae1202117eeeb02df51a7fae2ff0e065`

```dockerfile
```

-	Layers:
	-	`sha256:880c55f634d48ce94ad3bb8cacfc7078eb2e41218f7962f3eaa30b355adff1cb`  
		Last Modified: Tue, 25 Feb 2025 23:58:49 GMT  
		Size: 6.4 MB (6359215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00adddef6b121ce63e94c60d5ab2016245da74390e08971f62258b1b0b12d528`  
		Last Modified: Tue, 25 Feb 2025 23:58:48 GMT  
		Size: 22.1 KB (22070 bytes)  
		MIME: application/vnd.in-toto+json
