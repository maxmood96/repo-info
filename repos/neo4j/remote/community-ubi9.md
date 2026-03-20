## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:3621535d1c445327f9cb7e11b4b0b63e453808967e455644bd2e4dc197d22df8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f50a8486d326796141e765e0e9415ce02ccfccbdbb5d37269a55fb2b11d2828a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386379741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76eea90acbf009fcf6923803a4c9f5f875a07b68f4f4a8b5ce784968f4e2063c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 17:49:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 17:49:40 GMT
ENV NEO4J_SHA256=63d4382d553d2d159e2da4c10a37a46f635e0a4418c5dac75887f7c88911823b NEO4J_TARBALL=neo4j-community-2026.02.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 20 Mar 2026 17:49:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.3-unix.tar.gz
# Fri, 20 Mar 2026 17:49:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 20 Mar 2026 17:49:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 20 Mar 2026 17:49:45 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:49:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 20 Mar 2026 17:49:45 GMT
VOLUME [/data /logs]
# Fri, 20 Mar 2026 17:49:45 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 20 Mar 2026 17:49:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:49:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f495377f935b0723f170550d361c1979e4a8a817d276b8cc53494559af9d9b1f`  
		Last Modified: Fri, 20 Mar 2026 17:50:08 GMT  
		Size: 94.3 MB (94259532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2cbe77697a41a16111be8602fa7a8237b6ffa5535afe2eb28b10b2d73b2b56`  
		Last Modified: Fri, 20 Mar 2026 17:50:05 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d2e1e214a7fac60c1da01dc4989e30748210c6c075a65fef73d959b1155621`  
		Last Modified: Fri, 20 Mar 2026 17:50:11 GMT  
		Size: 252.1 MB (252078881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5365e8aebe8259a60a76eae5bb87846fa939d4d771d20fb3d078e734c8030b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b35709eb28a451af1f35c91c15b0ef966bd955de1b7f4b0fcc53d8d20ce41a8`

```dockerfile
```

-	Layers:
	-	`sha256:88363d54dc2effa8ce713fdc4a23881691a3bcecef3137f5084d4e858990f630`  
		Last Modified: Fri, 20 Mar 2026 17:50:05 GMT  
		Size: 3.9 MB (3939605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1425f341ba893855ce91055f2e3381ac7056d5822ddb24f90a5e424d7805afa7`  
		Last Modified: Fri, 20 Mar 2026 17:50:05 GMT  
		Size: 21.5 KB (21531 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5bbf28e713bc6184c09dd383913307d82347ca0c5bd212a06ef3ed90579e403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.7 MB (383674640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97c01df7cee7e13259af73740ca0cd1211ccd6f092f73560cf834f067ddbe67`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 17:52:43 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 17:52:44 GMT
ENV NEO4J_SHA256=63d4382d553d2d159e2da4c10a37a46f635e0a4418c5dac75887f7c88911823b NEO4J_TARBALL=neo4j-community-2026.02.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 20 Mar 2026 17:52:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.3-unix.tar.gz
# Fri, 20 Mar 2026 17:52:44 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 20 Mar 2026 17:52:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 20 Mar 2026 17:52:49 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:52:49 GMT
WORKDIR /var/lib/neo4j
# Fri, 20 Mar 2026 17:52:49 GMT
VOLUME [/data /logs]
# Fri, 20 Mar 2026 17:52:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 20 Mar 2026 17:52:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:52:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d3277bfcd6f2cc8139dedef51eebbc687602074754b36ff87fc54ef582553`  
		Last Modified: Fri, 20 Mar 2026 17:53:15 GMT  
		Size: 93.4 MB (93380633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135fee40f84c7a241577d2664830c301a4c1e25621b3044e2bfb4404970b77a6`  
		Last Modified: Fri, 20 Mar 2026 17:53:10 GMT  
		Size: 10.2 KB (10180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3504a564732f09d6c0973875fb575ae36c0735de94fb543b16cc0aa5a311ce`  
		Last Modified: Fri, 20 Mar 2026 17:53:17 GMT  
		Size: 252.1 MB (252078893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:840cc5d75ca6cf2c050e53784d289450d7af4f31a95db9f9c8243280d9fde164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce74da54ff39cf830659156cc4a487742dfdc9a705a86f7d6d13cf939dac0f31`

```dockerfile
```

-	Layers:
	-	`sha256:bc49013397930b8515ccff3aada2100046b4bd98a686558b1666511c37b498c6`  
		Last Modified: Fri, 20 Mar 2026 17:53:11 GMT  
		Size: 3.9 MB (3937651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee79b58594e76f180cb28344bbe6c379f4e1b04d150f88a896e9493945e5c994`  
		Last Modified: Fri, 20 Mar 2026 17:53:10 GMT  
		Size: 21.7 KB (21692 bytes)  
		MIME: application/vnd.in-toto+json
