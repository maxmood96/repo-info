## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:e686ab5696bbc76516841aba2c86b5c76de270815d802e38b53b14a4ec7c2e06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:b3ed65852eb91c55bed4f33fe3756217f110b4e3ff42ee5d87f0400f171b6599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.2 MB (610152898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97feac930e127309ffb12239ea6eb80200fbd5466cc5a3d923e4551ad1ed9b5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL url="https://www.redhat.com"
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 05 Feb 2025 12:33:33 GMT
ENV container oci
# Wed, 05 Feb 2025 12:33:33 GMT
COPY dir:0423d0cd4a34047821e55a2806cb02fc682f017fba03e4344223878a61041986 in / 
# Wed, 05 Feb 2025 12:33:33 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 12:33:33 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 12:33:33 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL "build-date"="2025-02-13T04:19:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Wed, 05 Feb 2025 12:33:33 GMT
RUN /bin/sh
# Wed, 05 Feb 2025 12:33:33 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV NEO4J_SHA256=df89af2f412ae2b200c47dec0dff0d5381880e49f314112544817bc151dfbfcc NEO4J_TARBALL=neo4j-enterprise-2025.01.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 12:33:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
# Wed, 05 Feb 2025 12:33:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:33:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 12:33:33 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 12:33:33 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 12:33:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 12:33:33 GMT
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
	-	`sha256:449159284e3a74dd368edd6d145b63b6401596838323908ebef4d58a6fa0b402`  
		Last Modified: Fri, 14 Feb 2025 00:28:42 GMT  
		Size: 140.5 MB (140494784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0678b2557f97ce516ac1bcc6519346d19677c253520c006507f1856dc9e7dba9`  
		Last Modified: Fri, 14 Feb 2025 00:28:39 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba102ff0718d540867a5d2cacbca6ac31a9a2b81a9944f954fa308b669accd`  
		Last Modified: Fri, 14 Feb 2025 00:28:46 GMT  
		Size: 430.3 MB (430281035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c07b51eb61cfb3f6f68c272cf21f1f81a32d5b640928fcce61d25d6d91771382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6697422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ecb2ceebd7997f0cca63f560ab3f88753dd7a7f297f79ab49729882ccb5f86`

```dockerfile
```

-	Layers:
	-	`sha256:ca42dde97fa41ae857e625968c3705b8e4e052a820cf61730cb81b7f3ef041c4`  
		Last Modified: Fri, 14 Feb 2025 00:28:39 GMT  
		Size: 6.7 MB (6676022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4811c3f7a275c6a2ca9025a5508e1c180d0c9101cce26be61f45b8923b9edd4c`  
		Last Modified: Fri, 14 Feb 2025 00:28:39 GMT  
		Size: 21.4 KB (21400 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fbfb5cbc5b5025e0dcc709340dd4b059c69a10f13e353fe883deb238b4b7edcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608083166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2ef1c76a313423e6c082298e0603a66f1231f2265e5dfbbb1322b2bb1471ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL url="https://www.redhat.com"
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 05 Feb 2025 12:33:33 GMT
ENV container oci
# Wed, 05 Feb 2025 12:33:33 GMT
COPY dir:5809c16e2c5c048de6a8d8eea9437ac183b7d2503e26b24a2422ead5736aecad in / 
# Wed, 05 Feb 2025 12:33:33 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 12:33:33 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 12:33:33 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL "build-date"="2025-02-13T04:25:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Wed, 05 Feb 2025 12:33:33 GMT
RUN /bin/sh
# Wed, 05 Feb 2025 12:33:33 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV NEO4J_SHA256=df89af2f412ae2b200c47dec0dff0d5381880e49f314112544817bc151dfbfcc NEO4J_TARBALL=neo4j-enterprise-2025.01.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 12:33:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
# Wed, 05 Feb 2025 12:33:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:33:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 12:33:33 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 12:33:33 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 12:33:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 12:33:33 GMT
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
	-	`sha256:ea6f4f014076180b9e45fcebeadb8d71368d1da001ac26cf6d98b246e2912391`  
		Last Modified: Fri, 14 Feb 2025 01:18:43 GMT  
		Size: 140.2 MB (140165565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde90c25a51a1ac84158d0a0b0b017bea8d1f3369ffa21f37244ebf056ac39`  
		Last Modified: Fri, 14 Feb 2025 01:18:40 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7e014173c0956fa34c2ebbb0f87487ff5a9d8bf1f4abb6e9f25b48fcc21142`  
		Last Modified: Fri, 14 Feb 2025 01:20:05 GMT  
		Size: 430.3 MB (430281021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5bfaf67b2c678328dd35c66e2eaa9c7926495c1da0ffacfc2ba76383c94fee73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793d486c95da2d05e68896162a79afa3f322597ff1fa5f964b085466fa899106`

```dockerfile
```

-	Layers:
	-	`sha256:6276adcf5db7221638a0c9151f3a1e12519e0e74f04b3ad5b48e695822da132a`  
		Last Modified: Fri, 14 Feb 2025 01:19:57 GMT  
		Size: 6.7 MB (6655412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5981f4822bc3e1bddc010a33bcbf676adcae1a29d81fdea92a3f99742c88088`  
		Last Modified: Fri, 14 Feb 2025 01:19:56 GMT  
		Size: 21.5 KB (21513 bytes)  
		MIME: application/vnd.in-toto+json
