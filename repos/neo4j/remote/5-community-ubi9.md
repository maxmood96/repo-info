## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:9f173c02634cc74be3596f71fc6ce74ad334c681bdd04c839de46c12ba5a323f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c457fd98469d4e86b4f23391e641c5f2bb436d34cf680820492c9eba35214a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337202676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b572835e0aca740edc683c2274ea23f01b8fd310601360fa63219bd6f49fbe6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 14 May 2025 10:36:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 14 May 2025 10:36:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:36:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:36:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:36:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:36:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:36:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 14 May 2025 10:36:11 GMT
ENV container oci
# Wed, 14 May 2025 10:36:11 GMT
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Wed, 14 May 2025 10:36:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:36:11 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:36:11 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:36:12 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Mon, 09 Jun 2025 10:01:35 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV NEO4J_SHA256=150869beb82a7e8e2a093af086289a78cfb0e3c43f0076af535861085cb2bd50 NEO4J_TARBALL=neo4j-community-5.26.8-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Jun 2025 10:01:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.8-unix.tar.gz
# Mon, 09 Jun 2025 10:01:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.8-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 10:01:35 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Jun 2025 10:01:35 GMT
VOLUME [/data /logs]
# Mon, 09 Jun 2025 10:01:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Jun 2025 10:01:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Jun 2025 10:01:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135ffbfa940d24363e5aaf493636838d2361a4398aa9e7787431a40b93e45c6a`  
		Last Modified: Tue, 10 Jun 2025 00:07:31 GMT  
		Size: 129.5 MB (129452816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eda0b788c4d76f82ee701efced7c431df1e12fe2ff8bbe74b9f97d400700a2`  
		Last Modified: Mon, 09 Jun 2025 21:43:38 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb67b4e54392730f9a642a45ff35272695c0888c23da5086e985ff4515d40e9`  
		Last Modified: Tue, 10 Jun 2025 00:07:32 GMT  
		Size: 168.1 MB (168094699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d39a8cb001f191b151264f7853c675210ca70f0de5311c8ecdd24a79787341e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f7ba0c740ef189d9e62c81888253eab5cef5e4ba4caee96a4e15b48cb692f2`

```dockerfile
```

-	Layers:
	-	`sha256:a66d440298162584dd28825fa9843d1f1382a5ca0cc5cf40e4dc8b09e6b61203`  
		Last Modified: Mon, 09 Jun 2025 23:43:47 GMT  
		Size: 5.6 MB (5602372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb543ad1592eeb463c147c144d283b8b2942ff817c9a479657b635f527fc79ab`  
		Last Modified: Mon, 09 Jun 2025 23:43:48 GMT  
		Size: 21.2 KB (21163 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:af31386fe83c19af5fb2a95b7bcd40abd2e5f40e3e4fa108ef554ae3ca64a647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330373953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dacdaeefcdff279c44009f916e5082bb55367aa9eea9b07fbe845a8aa9bb61`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 14 May 2025 10:40:48 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 14 May 2025 10:40:48 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:40:48 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:40:48 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:40:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:40:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:40:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 14 May 2025 10:40:48 GMT
ENV container oci
# Wed, 14 May 2025 10:40:49 GMT
COPY dir:3fa6b42aa9cb1575a22397e201df9f16228db85fb99450db2e9f8bef40a52c0f in / 
# Wed, 14 May 2025 10:40:49 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:40:49 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:40:50 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:40:50 GMT
LABEL "build-date"="2025-05-14T10:40:32" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Mon, 09 Jun 2025 10:01:35 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV NEO4J_SHA256=150869beb82a7e8e2a093af086289a78cfb0e3c43f0076af535861085cb2bd50 NEO4J_TARBALL=neo4j-community-5.26.8-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Jun 2025 10:01:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.8-unix.tar.gz
# Mon, 09 Jun 2025 10:01:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.8-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 10:01:35 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Jun 2025 10:01:35 GMT
VOLUME [/data /logs]
# Mon, 09 Jun 2025 10:01:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Jun 2025 10:01:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Jun 2025 10:01:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9cf99093c2fb01ee3da769d664a9212c42b7d50516f9e77975132a6540ccdf3b`  
		Last Modified: Thu, 15 May 2025 19:25:04 GMT  
		Size: 37.9 MB (37876105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665d1fd9fc1b5f90e9979d5b2f2c44318b291c5fca5c36b2dc7a2547c6a4ccb3`  
		Last Modified: Wed, 04 Jun 2025 21:01:41 GMT  
		Size: 124.4 MB (124392983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3277e38f74eb58b28b880db5c1eae942675948cc26eb06ce175cf113e27492`  
		Last Modified: Wed, 04 Jun 2025 21:01:30 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4114c8aa6216f51cf601ce1fdc193b06327c6946771f5bf0b86ef0589d026356`  
		Last Modified: Tue, 10 Jun 2025 00:07:33 GMT  
		Size: 168.1 MB (168094807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f1ddc3a46279611c5796e5acc48c189df0ec2264cbfdcd2d5b373ce65a222ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e429e26990b41d448cb5a88d9059b9081a78192d60729cfe81f32f85a0cb10`

```dockerfile
```

-	Layers:
	-	`sha256:76cda894af15992b5e6c5d929c95e0e76906f756b736ba1870e6bc0467c822c3`  
		Last Modified: Mon, 09 Jun 2025 23:43:53 GMT  
		Size: 5.3 MB (5264294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe0632e03285320f6a582f54daa8e4ad52cb8547a0152028d1ddf0db8bdf8cd`  
		Last Modified: Mon, 09 Jun 2025 23:43:53 GMT  
		Size: 21.3 KB (21300 bytes)  
		MIME: application/vnd.in-toto+json
