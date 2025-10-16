## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:fd3ab64dd5daa4444a29e33ca08b02e88faa39e4edfb7403813dde751d5634e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:49376ddd2d823aa86d90b8d72ce9f482e0716a678e2f22d8393186260f24347b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.9 MB (512888095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb8941e6cbcd42010ca68c943e1d16ab0abb666a2390f9027cbd9ac09767142`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 30 Sep 2025 13:19:30 GMT
ENV container oci
# Tue, 30 Sep 2025 13:19:30 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Tue, 30 Sep 2025 13:19:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:19:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 30 Sep 2025 13:19:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 30 Sep 2025 13:19:30 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Tue, 30 Sep 2025 13:19:30 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV NEO4J_SHA256=0b81f4601987925d0a7a844b4206fc75fefb8cd989bc95b00f1ecbf38afc3e4f NEO4J_TARBALL=neo4j-enterprise-2025.09.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201f13f2dc417d5fc36f8a55a1f9ec096ed52dddac9bf07a97464d388e2232e`  
		Last Modified: Thu, 16 Oct 2025 20:11:05 GMT  
		Size: 131.3 MB (131303044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b526588bf52987d01193c7cd2e4a7edb2cb68c63559e63f7846a8534f03ae5`  
		Last Modified: Thu, 16 Oct 2025 19:29:14 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cc1ad527ca56141b5d44f13a73f913b32707c83bc86d3e1f37fa7c6c838801`  
		Last Modified: Thu, 16 Oct 2025 20:11:06 GMT  
		Size: 341.9 MB (341921473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d64788627a56bf93fd6cae64d11bc14ce4332ba592915cb536ff3686cb8b41ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee0eff0b735b55f4bbf7f58f07500b4a94c7b37f9520e1af3a147957dd992d4`

```dockerfile
```

-	Layers:
	-	`sha256:c5a7c999a588ba78745e5c0f44c055d61be6d83134a82c01bd52de5b39cc217b`  
		Last Modified: Thu, 16 Oct 2025 20:43:29 GMT  
		Size: 5.6 MB (5610293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96eef55766bc6b6b0b506128ca61ed760d9f56b038f06f8e7293d2d35738705a`  
		Last Modified: Thu, 16 Oct 2025 20:43:31 GMT  
		Size: 20.7 KB (20660 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0be70d4cc13dc281a0e3803645b495350166a6b0e9cb4880537f78d2eb28dc9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.8 MB (510758067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bd576347ef50d33623070564d895ec3cfd944f34b66eeb9a26e52a5c1d59a9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 30 Sep 2025 13:19:30 GMT
ENV container oci
# Tue, 30 Sep 2025 13:19:30 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Tue, 30 Sep 2025 13:19:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:19:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 30 Sep 2025 13:19:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 30 Sep 2025 13:19:30 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Tue, 30 Sep 2025 13:19:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Tue, 30 Sep 2025 13:19:30 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV NEO4J_SHA256=0b81f4601987925d0a7a844b4206fc75fefb8cd989bc95b00f1ecbf38afc3e4f NEO4J_TARBALL=neo4j-enterprise-2025.09.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d7f7a78b84860c60ce67d05fe45caa2904db19aa21cc750f859e267080ed64`  
		Last Modified: Thu, 16 Oct 2025 19:29:00 GMT  
		Size: 130.9 MB (130930292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb3311d22ab3f351c60cf7582230e812ac17f4bbb2a4608d3ed5c42edcdbd08`  
		Last Modified: Thu, 16 Oct 2025 19:29:13 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f147feacafb44c15af69d5bbd59abd3c6896a71a02fb3bff2835f7cbef22e7c8`  
		Last Modified: Thu, 16 Oct 2025 19:29:05 GMT  
		Size: 341.9 MB (341921441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0e0d4c1b2d676cf00a340278c293dbd0db9842b5ab8acdf9af46ca9dacefaeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5610810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446cf82e14dbf3acc157374d59061e79a6b1e7065765774565deca3ffe522751`

```dockerfile
```

-	Layers:
	-	`sha256:3b4f062375ec4a288365b069db0bd23602512a7a3f93072abf5c8453f023ca77`  
		Last Modified: Thu, 16 Oct 2025 20:43:37 GMT  
		Size: 5.6 MB (5590037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f702120c588d9e23c5ea75def3ebca14f497a94cab72dd761527a2a6da6205e6`  
		Last Modified: Thu, 16 Oct 2025 20:43:38 GMT  
		Size: 20.8 KB (20773 bytes)  
		MIME: application/vnd.in-toto+json
