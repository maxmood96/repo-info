## `neo4j:2025-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:32d1cbcb86795d38edd1e19264818f33d53beae287a58b3323a25ff7ddb89762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:1c4ddf9ab28b410ba06dc351f67f38c01afa447b8b09372fc14ad40753fd0c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.0 MB (614010573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50f9b47bda328b0b4c8e97b4e1adefbdadee1b308acc149f9422c097af3e4a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL url="https://www.redhat.com"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.openshift.expose-services=""
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 27 Feb 2025 14:20:06 GMT
ENV container oci
# Thu, 27 Feb 2025 14:20:06 GMT
COPY dir:15b23b07af120e2e0a5f4d490f44d738ca8fb631feddbf3564dd5d54104ea356 in / 
# Thu, 27 Feb 2025 14:20:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 14:20:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL "build-date"="2025-03-13T07:20:00" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 27 Feb 2025 14:20:06 GMT
RUN /bin/sh
# Thu, 27 Feb 2025 14:20:06 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV NEO4J_SHA256=d4323822935d7677ae5a12dd5638a1ed7012c190b6dd93913640ac2fda30501f NEO4J_TARBALL=neo4j-enterprise-2025.02.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Feb 2025 14:20:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
# Thu, 27 Feb 2025 14:20:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 14:20:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Feb 2025 14:20:06 GMT
VOLUME [/data /logs]
# Thu, 27 Feb 2025 14:20:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Feb 2025 14:20:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:533b69cfd644e5f3e5bde1a8c302567c595a28af93b9318ac6a3e9394740fb4d`  
		Last Modified: Thu, 13 Mar 2025 08:27:55 GMT  
		Size: 39.4 MB (39359404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863e9a7e21028fb223595c360e0b25839f814e468af01725b95defa89bd29b53`  
		Last Modified: Thu, 13 Mar 2025 08:27:58 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a23c36f1a42fa191b385f073f83511f1a602c5118be023c0242c42472e1fbc`  
		Last Modified: Thu, 13 Mar 2025 22:36:11 GMT  
		Size: 140.5 MB (140486644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a464e4d0282aa0d80425eee3bdda6fcf1654d75b5d35f62451faca40c728ba`  
		Last Modified: Thu, 13 Mar 2025 22:36:07 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c8312a4c4741a2b9cde9c921724683728c610015bf87639c4e72ecc4e865e0`  
		Last Modified: Thu, 13 Mar 2025 22:36:14 GMT  
		Size: 434.2 MB (434154002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d3f11871162ee22cd3a91ff33a88cea2a530d301980bf1c1358605092cf7d000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6696022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447464030bee42ca9cf0e99d7f6125e4a48ac1555a1f53c6243479794f7d7c28`

```dockerfile
```

-	Layers:
	-	`sha256:ea9a9dced6eb53c6062c87e17414b6b2f4a9cdb9945f9dfba4f971a3a842d49e`  
		Last Modified: Thu, 13 Mar 2025 22:36:07 GMT  
		Size: 6.7 MB (6674622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72c772772cb051be6b45d3bdf95e26b92519d11fae37794e95d1ef17a459af1`  
		Last Modified: Thu, 13 Mar 2025 22:36:07 GMT  
		Size: 21.4 KB (21400 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76149f9d4071a9bdccae21fd33cab9b6e0f6679d866aad66421d310dd4c0fc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611927527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af5c338cc720675b1f569d5197254cafaedbd5d4db48e4dc0b0dd03080eb328`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL url="https://www.redhat.com"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.openshift.expose-services=""
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 27 Feb 2025 14:20:06 GMT
ENV container oci
# Thu, 27 Feb 2025 14:20:06 GMT
COPY dir:b7138ac36fc7710c19e28655d453b8712ae774de42fbfc7d7975b03b9664b7ae in / 
# Thu, 27 Feb 2025 14:20:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 14:20:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL "build-date"="2025-03-13T07:21:58" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 27 Feb 2025 14:20:06 GMT
RUN /bin/sh
# Thu, 27 Feb 2025 14:20:06 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV NEO4J_SHA256=d4323822935d7677ae5a12dd5638a1ed7012c190b6dd93913640ac2fda30501f NEO4J_TARBALL=neo4j-enterprise-2025.02.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Feb 2025 14:20:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
# Thu, 27 Feb 2025 14:20:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 14:20:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Feb 2025 14:20:06 GMT
VOLUME [/data /logs]
# Thu, 27 Feb 2025 14:20:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Feb 2025 14:20:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8f0b1160a7bdb1abc6f59217ba0a1ed1eb53a9ddbbcaddd95d709604e095f742`  
		Last Modified: Thu, 13 Mar 2025 08:37:12 GMT  
		Size: 37.6 MB (37590719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e019691d61a0d5163ed02fe7a0cee4161254fd2d91b44221c46f8f765e011b`  
		Last Modified: Thu, 13 Mar 2025 08:37:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bb08d17ce452fcc9b831191e2e6b0995d19997a034b52681bd4b9757d531c6`  
		Last Modified: Thu, 13 Mar 2025 23:02:28 GMT  
		Size: 140.2 MB (140172274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a698b36c5500400e806932d19e7ca93e3cc0d1dc078085663916f8eb7436a04`  
		Last Modified: Thu, 13 Mar 2025 23:02:23 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c592d731085675ca762bdc295d7871b79798d857fc78cde2698f765cce5fd751`  
		Last Modified: Thu, 13 Mar 2025 23:02:36 GMT  
		Size: 434.2 MB (434154012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b7b458b615cfa115523cc653417d3b38bfe71a4f52825f5dc2f7d34e4857ac5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa478c7ecf53faa2855772854f9f764b9b7e7d61f1e59d98920a8ee4bd0a065`

```dockerfile
```

-	Layers:
	-	`sha256:3112f49a0ad1eb46b368b7c27d8698f27bbc3119e7f888abb2d340cd2fb53789`  
		Last Modified: Thu, 13 Mar 2025 23:02:24 GMT  
		Size: 6.7 MB (6654012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb846d64dcbd521fdeecfc654f4a31525e800e1755709fca36438208fbfd0b4`  
		Last Modified: Thu, 13 Mar 2025 23:02:23 GMT  
		Size: 21.5 KB (21513 bytes)  
		MIME: application/vnd.in-toto+json
