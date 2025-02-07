## `neo4j:2025-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f1ffe9095a676544dc9b315381efd8e06343f4ab7f35cf0d6ef0866631f739b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c0e91828628b71874080ae3b7059aaad32b900169649735f3958c13f683d57ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.2 MB (610161827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa15e8d956c72a6439b9b947b4a4fe0b4958552d95fe0d3113b2b5a73ac822c`
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
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Wed, 05 Feb 2025 12:33:33 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 12:33:33 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 12:33:33 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
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
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:31:07 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:31:05 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961de59befae99c606bac03ad0dd6c2dee8e7f5058c48d5da3c812171fedb19`  
		Last Modified: Fri, 07 Feb 2025 00:31:47 GMT  
		Size: 140.5 MB (140500034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a0f7c8f7604a033c5ba2aea7dd020b98d881f4b6a89c165fd48592c1878a8f`  
		Last Modified: Fri, 07 Feb 2025 00:31:43 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1b45d125a71f54837b5b7c4579a8f04b38c18c67ab46a2842b2a24d920b86a`  
		Last Modified: Fri, 07 Feb 2025 00:31:53 GMT  
		Size: 430.3 MB (430280999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17e473107ac180f3447136ef162935daebca44296bf3e6917300c92f23b6a5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6697390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9b196932cd5867fd81baf4583e89093a6dd19db048cd1b58a75f7e972eae5e`

```dockerfile
```

-	Layers:
	-	`sha256:aab4daf6e3b19acd591057120300766ccbea7045bc065c9015640b6557c89cb9`  
		Last Modified: Fri, 07 Feb 2025 00:31:43 GMT  
		Size: 6.7 MB (6675990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb419d070f3f2fef7555ba0d959af7e4eb193653e3a6b0cf019c97f18ebc3ea9`  
		Last Modified: Fri, 07 Feb 2025 00:31:43 GMT  
		Size: 21.4 KB (21400 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:65603e00b13e358e9fe816ab92648a0452f742407400fcf0d07b745df820e638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608057084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432266c11e74b7196946465ea519ea5a89f8bdfa41bc742d612ba61186ad4c8d`
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
COPY dir:389f5f73f217a50cb052c224af980ef5943f8527170a8ed8ba3b540101351720 in / 
# Wed, 05 Feb 2025 12:33:33 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 12:33:33 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 12:33:33 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 12:33:33 GMT
LABEL "build-date"="2025-02-06T04:48:45" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
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
	-	`sha256:8174eb1151f28d1a88085da5d27ffd5729467439a2f1a77d03498e89f9f7ef4b`  
		Last Modified: Thu, 06 Feb 2025 05:31:06 GMT  
		Size: 37.6 MB (37592304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c4d65a5f9a8b0c8f76083cf10d14a2417324b530dfde1115d46147afe1c17`  
		Last Modified: Thu, 06 Feb 2025 05:31:05 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc415c6a77a7fb894e89e695b018c6295b45502af3a20f7c732921ce7d6fec`  
		Last Modified: Fri, 07 Feb 2025 02:38:37 GMT  
		Size: 140.2 MB (140173178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2358ab889a07ad4b20d6e4080254c5fd0669e19b12100145e0d72e8b2f65a3c0`  
		Last Modified: Fri, 07 Feb 2025 02:38:33 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f561b3b7a980b7db491c26e427909489ecfa3712603384ca5c67d2c8a20db167`  
		Last Modified: Fri, 07 Feb 2025 03:46:03 GMT  
		Size: 430.3 MB (430281078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a5651b0cf3d5a635892e20dfdab0f94151899f271c1aee9154efaecdefabe6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2675b70cf10fde5fc01a2d7d37e2ae63f93dc9d972ab1dbd45e3fbc081bd45`

```dockerfile
```

-	Layers:
	-	`sha256:f8c2d5951ce76e0ec4ae229729660ec8188a53c24e2fae4a89112eee02000fb0`  
		Last Modified: Fri, 07 Feb 2025 03:45:54 GMT  
		Size: 6.7 MB (6655368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1ace0ef8ea86243059bf74f323dc14316449bc7de45b1b8d87c0c585d5434c`  
		Last Modified: Fri, 07 Feb 2025 03:45:53 GMT  
		Size: 21.5 KB (21512 bytes)  
		MIME: application/vnd.in-toto+json
