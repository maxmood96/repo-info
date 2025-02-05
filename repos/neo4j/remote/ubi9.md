## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:86e58990534ac066611dfb90b742ba706f2f9bffdbccf472b08290d2cb1b7a21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:394fdc3938c6e19a27fbc9149ca66cfb7d2b4b2d219a5b5d5c1ed503d768a072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332215356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe06843cf6a27b8143d8b7851b5643ebae18362960d98b6f12d9c1c1e238ef5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL url="https://www.redhat.com"
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Jan 2025 15:28:28 GMT
ENV container oci
# Mon, 20 Jan 2025 15:28:28 GMT
COPY dir:791945992d1a1a0e69cb46f548168dd778c0a5b28228ca7d157145f53fdb49cd in / 
# Mon, 20 Jan 2025 15:28:28 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:28:28 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL "build-date"="2025-02-04T04:38:14" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
# Mon, 20 Jan 2025 15:28:28 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:24436b52f270faaf1cd45508746ed85af4420ecadbf33becda289f2e4221eb18`  
		Last Modified: Tue, 04 Feb 2025 06:12:46 GMT  
		Size: 39.4 MB (39370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7773c651ce2558c22521f6ea1bb2e11b3a7e0f291de522fb1183c6ab4e62c1a6`  
		Last Modified: Tue, 04 Feb 2025 06:12:45 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4123602346d7aba29cc9f6cf4fddad0a7a8c05d1b655263d41f325b58e08a`  
		Last Modified: Tue, 04 Feb 2025 20:34:38 GMT  
		Size: 133.9 MB (133854641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334a8fe5317f5f28088446d9f9ec1d8de20697fc69d2e91d4152e36b239fdb9b`  
		Last Modified: Tue, 04 Feb 2025 20:34:36 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e3112510e3a2b357d0ff21bf6e7ed3a4f09ed1de97b261b223d630c6bfe964`  
		Last Modified: Tue, 04 Feb 2025 20:34:39 GMT  
		Size: 159.0 MB (158979255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3e08f74c09a1fb6ebec31fac930c5a215fc5ee4028a47d3e571f8a2cc56f5199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6b019553865dfb4c5ba164855c7a7c239091d9e8b4d9acce9a3fecfa31bd2e`

```dockerfile
```

-	Layers:
	-	`sha256:6cef1c810d0fa767d892cbbba2d5053cf33dd2f9e490bf1b543cc8a871e3dfac`  
		Last Modified: Tue, 04 Feb 2025 20:34:36 GMT  
		Size: 6.4 MB (6375164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2729bcc9e55b37bc92c318a72d43de47d8f058fb6d32e8942a18a77b0c9e203`  
		Last Modified: Tue, 04 Feb 2025 20:34:36 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fd67e3c27dedfeea07f3883c8bbb3e655648369ae08a742c4b624656216fd3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330450187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4815d1332a3f31f436958425771c78977a2d81a876cb8031cb71b284977b5f4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL url="https://www.redhat.com"
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Jan 2025 15:28:28 GMT
ENV container oci
# Mon, 20 Jan 2025 15:28:28 GMT
COPY dir:9a473b4852f6cbe9a0f08b40d1fff87f485e10a0b3973b8009cae74075e5e063 in / 
# Mon, 20 Jan 2025 15:28:28 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:28:28 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 20 Jan 2025 15:28:28 GMT
LABEL "build-date"="2025-02-04T04:40:56" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
# Mon, 20 Jan 2025 15:28:28 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:93168a48887270ffcd74fa1e7b5a85a6420b35b7dca5a5971f063fb8a0d3264a`  
		Last Modified: Tue, 04 Feb 2025 06:12:53 GMT  
		Size: 37.6 MB (37592781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b362866ca09649c77058b63f51549ffa71c5ffce326fe4b42995cfb1180db`  
		Last Modified: Tue, 04 Feb 2025 06:12:52 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb8f4eff196eb1bff3f448ea7e6688d9e6438a2923867b63d9aa223a8c401a9`  
		Last Modified: Wed, 05 Feb 2025 02:49:24 GMT  
		Size: 133.9 MB (133867638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce5758258f346d485544f4e0d906588cd5636384bdd5757baf9fb0eb2b1bca`  
		Last Modified: Wed, 05 Feb 2025 02:49:21 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930bc950a105c17ba0117a2d232e97eb8bc7b17ebff2c30e250fda6b75ee63aa`  
		Last Modified: Wed, 05 Feb 2025 02:49:25 GMT  
		Size: 159.0 MB (158979244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d48209fbd3f1a751a4bfa4b7852bd6ddc33f5bd883c5ecc1769b67ac1e12e773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1120e800d99214902e4267e85a5780f28279ffec217ade4aed487edf17fb14`

```dockerfile
```

-	Layers:
	-	`sha256:864b6d815c4aaf9c311a855e8edf957a6e6398524feaf3b377f475955eff5669`  
		Last Modified: Wed, 05 Feb 2025 02:49:21 GMT  
		Size: 6.4 MB (6354588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c5bbad5a18d8f48220defa232f4fd7272c5cee11b82fcfd536ece5828bc1f1`  
		Last Modified: Wed, 05 Feb 2025 02:49:21 GMT  
		Size: 22.7 KB (22697 bytes)  
		MIME: application/vnd.in-toto+json
