## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:60ae456c53c12aa2789a5b779248014cb9dacc86f2c2ec6901613322298494d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c897871f4635aa3255e9d42cf1ef82a3cad4640ba12a4a5478e403af7432e78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290903371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d95e4af753974b82c1b8f488d564e7154a83e4188537847da90e0e294a9bca`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdeea4bff514734394ac4632b56f6b054270f23b05ec00a134dc8cd0a525709a`  
		Last Modified: Tue, 09 Jul 2024 18:58:53 GMT  
		Size: 125.1 MB (125067152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46257c64b914817f24d229e7bdae5b67a6ea69c07a79b8841c9c13a7675cf93b`  
		Last Modified: Tue, 09 Jul 2024 18:58:50 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c2e12b6000bad7929ff3b612e3ea3f929c44927610cf1c92e6effb205cf3a7`  
		Last Modified: Tue, 09 Jul 2024 18:58:52 GMT  
		Size: 127.0 MB (126974244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:300917907ddbfcdf7a233341d2872cbdc7426d1edf488ff6db4165afb83d282d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fa7350b42ddd227cfa11a1eb1afbdf3f1cf5e2f96e69a39ef5ab4a1d09141d`

```dockerfile
```

-	Layers:
	-	`sha256:a512d471ebbe685f28db4b3ad43d8a31fa08ebe5effbc10f0d812b240b0879e5`  
		Last Modified: Tue, 09 Jul 2024 18:58:51 GMT  
		Size: 5.1 MB (5052324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26975576211d506fd1bceaefa95f10b9fca6085ac4997bcd06efd4828b9c0d2`  
		Last Modified: Tue, 09 Jul 2024 18:58:50 GMT  
		Size: 21.7 KB (21721 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json
