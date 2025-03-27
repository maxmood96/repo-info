## `neo4j:2025-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:2866ae77b012a1ef5705852f867b225f028ff000df9cd342b11ee7ef47a87f6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:11ab66b69d5bdaec5ed54b23887cf69a095b9351100453c61615a9f66bd4a649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.9 MB (488912737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b509c7efe756d72d63f3ed5efdfb4b9a0f60135a86eb7088b9afd18fdc1b7ff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
# Thu, 27 Mar 2025 13:20:50 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV NEO4J_SHA256=39d74d8f0e1f6d31a3ab459a2548f8c66eff86678bb141572513c6f68f893d45 NEO4J_TARBALL=neo4j-enterprise-2025.03.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Mar 2025 13:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
# Thu, 27 Mar 2025 13:20:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:20:50 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Mar 2025 13:20:50 GMT
VOLUME [/data /logs]
# Thu, 27 Mar 2025 13:20:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Mar 2025 13:20:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Mar 2025 13:20:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5215c6b9dc26a9d39eac1f88d8b1566f11ef5c32321b128b8c27996d2d59bcf6`  
		Last Modified: Thu, 27 Mar 2025 18:59:28 GMT  
		Size: 131.0 MB (131026344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33f226b4d8da6bbdab672405b0aeea3f4ebd1cad162a312df41bd49ab657c2`  
		Last Modified: Thu, 27 Mar 2025 18:59:26 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cb6341347d0cc81baeebf3fd0b44cdd8803c460346401142c0b0eef552b6c1`  
		Last Modified: Thu, 27 Mar 2025 18:59:32 GMT  
		Size: 318.5 MB (318469856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaf3bc8cb940011698c6b98183e77ac3d8e1df92feb0ba5b8ec088ced51a4400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95620b3c92b0df433f04df38e8f90d0ce66e1c57063182223daee790fa4cc34`

```dockerfile
```

-	Layers:
	-	`sha256:6547b6d6817933d42b4688474ca7aefbe3de79260d53059c0c984d3e108c1201`  
		Last Modified: Thu, 27 Mar 2025 18:59:29 GMT  
		Size: 5.6 MB (5552472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15cf980b9e340b49d7b83f27fe6388a3ae6ab5402c07d82989ef76015a1180f2`  
		Last Modified: Thu, 27 Mar 2025 18:59:29 GMT  
		Size: 21.4 KB (21400 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b90b80db88d659e2bbff69672b24bea506b9149e162ae30af6fa0709d8e1e194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.7 MB (486715298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3631557efddbac9f3055c3fc128c97a87edaa2248101a35291ecb991e8b8c9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:05:13 GMT
ENV container oci
# Tue, 25 Mar 2025 15:05:14 GMT
COPY dir:36dabe56d778e21d6cac6872809f7ae0932c9956fe7621a40aed471a4eb28b35 in / 
# Tue, 25 Mar 2025 15:05:14 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:05:14 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:05:14 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:05:14 GMT
LABEL "build-date"="2025-03-25T15:04:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:05:25 GMT
RUN /bin/sh
# Thu, 27 Mar 2025 13:20:50 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV NEO4J_SHA256=39d74d8f0e1f6d31a3ab459a2548f8c66eff86678bb141572513c6f68f893d45 NEO4J_TARBALL=neo4j-enterprise-2025.03.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Mar 2025 13:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
# Thu, 27 Mar 2025 13:20:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:20:50 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Mar 2025 13:20:50 GMT
VOLUME [/data /logs]
# Thu, 27 Mar 2025 13:20:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Mar 2025 13:20:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Mar 2025 13:20:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7b061f511294c383e785796c55415ec3bed7fbb0a98d6cee8c8c6a1436d4ada8`  
		Last Modified: Tue, 25 Mar 2025 18:27:33 GMT  
		Size: 37.6 MB (37588703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6607d3dbc4fd04e0d544f944d20a47a5af1fa8a7520e1f37683ab236e23734`  
		Last Modified: Tue, 25 Mar 2025 18:27:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17c51be2b35101d5dd5924532f25040a589c34d2a2cabe0e509d4449d12a17d`  
		Last Modified: Thu, 27 Mar 2025 18:20:07 GMT  
		Size: 130.6 MB (130646184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b974208887f67d63c435521b956c03530f9629368df8016d00123453f2c024f`  
		Last Modified: Thu, 27 Mar 2025 18:20:03 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b589eae2951dd671e047f361ba0e4287a1b38be778faa58c9874c38c31dc2e79`  
		Last Modified: Thu, 27 Mar 2025 19:05:24 GMT  
		Size: 318.5 MB (318469897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1654d3a0e00f959bdb5376efb4cc68006a949946b9656d749e1d01490c180a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb377ccab5b4ae929d875fbc8fb524f08e718a31b6f0e363403db09b61e0161`

```dockerfile
```

-	Layers:
	-	`sha256:cffafca0bd6cbff9ba960c1487f69d21993d10279ff00036ce28a018e5b1bf5c`  
		Last Modified: Thu, 27 Mar 2025 19:05:15 GMT  
		Size: 5.5 MB (5531862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c248bb2d7a61eebfac598e1d99d0576ac79dc8efe748407ec30b2da50cccec9`  
		Last Modified: Thu, 27 Mar 2025 19:05:15 GMT  
		Size: 21.5 KB (21513 bytes)  
		MIME: application/vnd.in-toto+json
