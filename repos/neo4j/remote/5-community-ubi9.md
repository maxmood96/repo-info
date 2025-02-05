## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:784d718b132b81335ee83b8bb3479d8e5aea8bb455d34d9d06cc3df11daad674
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:899a10f368fea465848d078f11d760e2945a2dc15cb710a4c3e109f7d767293a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333531786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dae6720e254db79297de1bb6518c529ee54a193a750e47679fc95ceeab0e4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Feb 2025 04:38:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Feb 2025 04:38:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 04 Feb 2025 04:38:46 GMT
LABEL url="https://www.redhat.com"
# Tue, 04 Feb 2025 04:38:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 04 Feb 2025 04:38:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Feb 2025 04:38:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Feb 2025 04:38:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Feb 2025 04:38:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Feb 2025 04:38:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Feb 2025 04:38:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Feb 2025 04:38:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Feb 2025 04:38:47 GMT
ENV container oci
# Tue, 04 Feb 2025 04:38:48 GMT
COPY dir:791945992d1a1a0e69cb46f548168dd778c0a5b28228ca7d157145f53fdb49cd in / 
# Tue, 04 Feb 2025 04:38:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 04 Feb 2025 04:38:48 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 04:38:49 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 04 Feb 2025 04:38:49 GMT
LABEL "build-date"="2025-02-04T04:38:14" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
# Tue, 04 Feb 2025 04:39:05 GMT
RUN /bin/sh
# Wed, 05 Feb 2025 10:07:55 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
ENV NEO4J_SHA256=95dde4f8092b9dffb57f74248ef6579bc36d6418c07ba7c513d9c95a36f44518 NEO4J_TARBALL=neo4j-community-5.26.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 10:07:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
# Wed, 05 Feb 2025 10:07:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 10:07:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 10:07:55 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 10:07:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 10:07:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 10:07:55 GMT
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
	-	`sha256:7d911b0d88e6855d1cdc72f7cdfc65841a4904ea1b51b21674a27a13f1dbdb23`  
		Last Modified: Wed, 05 Feb 2025 19:28:37 GMT  
		Size: 133.9 MB (133854593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6bdffd2e3f8bcf3917c093ac546661202c66eb7b7039dca67ab1c632cf6767`  
		Last Modified: Wed, 05 Feb 2025 19:28:35 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4bd4f1c85791b8c46fdb2743db0a603fe758af1e135d4b0ace74a121efdea9`  
		Last Modified: Wed, 05 Feb 2025 19:28:38 GMT  
		Size: 160.3 MB (160295736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1fe9482ca8f87bfd15347c16f44104e8dc19e80bab9a1fd9ec3b1ad17b47d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6401703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d0f8ff0c06701bee6c0c4dc56df4602875a928a2fb51785257c24e701740cc`

```dockerfile
```

-	Layers:
	-	`sha256:73486f2aad7fe1db4021b7e96a71ef1a756d7c173ace63b344db33ba21949f21`  
		Last Modified: Wed, 05 Feb 2025 19:28:35 GMT  
		Size: 6.4 MB (6379771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edce7cc74c4c4afc3adced0483c911b5b5da24962a02dba3f55fc15caa0bd585`  
		Last Modified: Wed, 05 Feb 2025 19:28:35 GMT  
		Size: 21.9 KB (21932 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7a1758e94d83b9324faa3c3711785d4c170f3a044a6df080b05ccf7ad67f881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331766746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633c8320a267ebd65da0d1ff92e49b1b50174cdc45675397f9f4a7141cd5eb73`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL url="https://www.redhat.com"
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Feb 2025 04:41:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Feb 2025 04:41:21 GMT
ENV container oci
# Tue, 04 Feb 2025 04:41:22 GMT
COPY dir:9a473b4852f6cbe9a0f08b40d1fff87f485e10a0b3973b8009cae74075e5e063 in / 
# Tue, 04 Feb 2025 04:41:22 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 04 Feb 2025 04:41:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 04:41:23 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 04 Feb 2025 04:41:23 GMT
LABEL "build-date"="2025-02-04T04:40:56" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
# Tue, 04 Feb 2025 04:41:33 GMT
RUN /bin/sh
# Wed, 05 Feb 2025 10:07:55 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
ENV NEO4J_SHA256=95dde4f8092b9dffb57f74248ef6579bc36d6418c07ba7c513d9c95a36f44518 NEO4J_TARBALL=neo4j-community-5.26.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 10:07:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
# Wed, 05 Feb 2025 10:07:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 10:07:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 10:07:55 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 10:07:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 10:07:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 10:07:55 GMT
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
	-	`sha256:5c0754c6e3be77a4d9a3b8b042aca50f9f7546db33e2463afd47f2f8a218627a`  
		Last Modified: Wed, 05 Feb 2025 19:36:18 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67118310c084cae30743139250ec4de92c5a21fa15a6860a9f7c59436a4a70fa`  
		Last Modified: Wed, 05 Feb 2025 19:36:22 GMT  
		Size: 160.3 MB (160295805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c266868cca0a4eb60ad9c3b2c941a61fb609998fda31fa6005166943603dbce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efe173d10794dc893b5882ad722f0dbb362b3d6c7d2699a9eae07208b6b5c98`

```dockerfile
```

-	Layers:
	-	`sha256:16f95fd41f70443b902e8406f84d9249c4b9bb2bff1e2ddb89e3f768b9fce461`  
		Last Modified: Wed, 05 Feb 2025 19:36:19 GMT  
		Size: 6.4 MB (6359171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51933a0451061695afc3e39021c6814968a36a374de7cf351887b4bbb3e571b`  
		Last Modified: Wed, 05 Feb 2025 19:36:18 GMT  
		Size: 22.1 KB (22070 bytes)  
		MIME: application/vnd.in-toto+json
