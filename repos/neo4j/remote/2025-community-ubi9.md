## `neo4j:2025-community-ubi9`

```console
$ docker pull neo4j@sha256:a8fe641d3aabcb662e7c0da6152a75cb5477b32d79ef6f92672dccfa67d590bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:44406e2f05f6c62991b34e0ec5dc49027843d85818dd482c0de9daf39d6ee6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376875190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ee68374681094f525f9c194262778d425baf7d366cd6a2230d22b88998ccef`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 00:42:56 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:42:56 GMT
ENV NEO4J_SHA256=69ade165e3347a132dea6664fce7fda86f391a7aefb1ab00f21ce940ea692f09 NEO4J_TARBALL=neo4j-community-2025.10.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 02 Dec 2025 00:42:56 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
# Tue, 02 Dec 2025 00:42:56 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 02 Dec 2025 00:43:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 02 Dec 2025 00:43:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:43:01 GMT
WORKDIR /var/lib/neo4j
# Tue, 02 Dec 2025 00:43:01 GMT
VOLUME [/data /logs]
# Tue, 02 Dec 2025 00:43:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 02 Dec 2025 00:43:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:43:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce98e9212338109659790b5890894d4932981fe4cfe3917d65de671a1b5b8a0`  
		Last Modified: Tue, 02 Dec 2025 05:04:02 GMT  
		Size: 131.3 MB (131300464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d5c9dd3f83008de9aca83eaa9646237f8604e0057e5d0271e68dbcd7178042`  
		Last Modified: Tue, 02 Dec 2025 00:43:45 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c22218530d86ffa9eda077f9cf3a26997bc3556aa0e88a49e62f6c1f0deb1a`  
		Last Modified: Tue, 02 Dec 2025 03:44:58 GMT  
		Size: 205.5 MB (205524589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:689863d16315dbd1b7891c37fc559dd39a83b634bbb5456120461c3fe160607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2faa003a2ca403c62c664978386164064f6d42fd8095c2bcf899b116fe657c5f`

```dockerfile
```

-	Layers:
	-	`sha256:3dd145d4b51eae9ff737d6cece964dc77405ccac95f7e033d58d7688952a04b8`  
		Last Modified: Tue, 02 Dec 2025 03:43:25 GMT  
		Size: 5.4 MB (5384778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62729d67b881b180e13d5b96988eb47bd9d52b348a11559e00511f2c53d25fab`  
		Last Modified: Tue, 02 Dec 2025 03:43:26 GMT  
		Size: 21.8 KB (21812 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a2086de602fbe1e025bf3de61aab4e6b7786eb97739ff4eb58c4c9560f928e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.7 MB (374693080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3959f68fe95f24760fa345dcc1fbe2c3aee49807e08c034165037d26cdc1f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 00:46:16 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:46:16 GMT
ENV NEO4J_SHA256=69ade165e3347a132dea6664fce7fda86f391a7aefb1ab00f21ce940ea692f09 NEO4J_TARBALL=neo4j-community-2025.10.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 02 Dec 2025 00:46:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
# Tue, 02 Dec 2025 00:46:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 02 Dec 2025 00:46:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 02 Dec 2025 00:46:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:46:20 GMT
WORKDIR /var/lib/neo4j
# Tue, 02 Dec 2025 00:46:20 GMT
VOLUME [/data /logs]
# Tue, 02 Dec 2025 00:46:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 02 Dec 2025 00:46:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:46:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4900c592012d50ea4b06130f7466a882754eb595de4a9ecfe132854df3755c5d`  
		Last Modified: Tue, 02 Dec 2025 03:44:34 GMT  
		Size: 130.9 MB (130936689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425ce7247406b7b34c8858921aafc8b39b494ab09c7acf51cef8279550073ecb`  
		Last Modified: Tue, 02 Dec 2025 00:46:57 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615cf480b379e6b98d6f7cdcbcdc0f1a8ce56815fbfd1122c9565740e3b598c6`  
		Last Modified: Tue, 02 Dec 2025 03:44:38 GMT  
		Size: 205.5 MB (205524632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:010ede8c2a50c16cc2ebf054ebc8039e0675bf923e3b6c961dbd7fdb511ae25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5386536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4763233582f458d7e26e6fea504e647255121a57ea67b4cc273ec7fdb844708f`

```dockerfile
```

-	Layers:
	-	`sha256:8d30124d638a3f0a7688dfc950ae3f9f8d469e313f6fb2fddfbb5639685b72dc`  
		Last Modified: Tue, 02 Dec 2025 03:43:31 GMT  
		Size: 5.4 MB (5364563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5120aedf5dde3150b2c2174318c7ab260c224fb58a65706498b366e9047652bd`  
		Last Modified: Tue, 02 Dec 2025 03:43:32 GMT  
		Size: 22.0 KB (21973 bytes)  
		MIME: application/vnd.in-toto+json
