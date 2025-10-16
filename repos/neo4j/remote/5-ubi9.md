## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:3e794232b506e949678f8fa155a28fcb7f835181b71665f16377cf6143a27c4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:eefd4d24330987ed7f316cc69d1281018cf9639a461724fdbfaaebe33a211d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286900841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fd3bcff3d698b8cf9782502b4b385ba9343fdee3c8bc95f5a10d72c4f0ea71`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 07:06:58 GMT
ENV container oci
# Mon, 06 Oct 2025 07:06:58 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 07:06:58 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 07:06:58 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 07:06:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 07:06:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 07:06:58 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 07:06:58 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV NEO4J_SHA256=670888ac88010ddb09df8a82b3f9f3552f03b16e8197e5855110aac86fe36f35 NEO4J_TARBALL=neo4j-community-5.26.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 06 Oct 2025 07:06:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
# Mon, 06 Oct 2025 07:06:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 07:06:58 GMT
WORKDIR /var/lib/neo4j
# Mon, 06 Oct 2025 07:06:58 GMT
VOLUME [/data /logs]
# Mon, 06 Oct 2025 07:06:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 06 Oct 2025 07:06:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 07:06:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3bd52c3f580e739d1e4793c49a14310e4de1c1e9d9826be12ee8eb30db5f1f`  
		Last Modified: Thu, 16 Oct 2025 19:29:26 GMT  
		Size: 124.6 MB (124614688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65d29691b56c52bfb12f0046866894c87408639cf44e42ea430410e3cdb8c3d`  
		Last Modified: Thu, 16 Oct 2025 19:29:14 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a857f6acf0213ff0f069618e5cc4a104837709de74870dcfeefd01cc0d89cbf`  
		Last Modified: Thu, 16 Oct 2025 19:29:28 GMT  
		Size: 122.6 MB (122622534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:cd8d106348de43246625547791d07003db00f40909c8c0d551e207a3d0ff3dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1503e39df40284f93beb63c3ee74568318750a7f0993d93cc9c2e2cfea73ba`

```dockerfile
```

-	Layers:
	-	`sha256:feb518cfad6a68f5ab9f28cef6357b65fc854fdc7eb4fb75eda80a1ddd72df1f`  
		Last Modified: Thu, 16 Oct 2025 20:44:02 GMT  
		Size: 5.3 MB (5250031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3197b18ac500b3f9a16d5b96ddaa7d5788b13e18be4d338b133aee81d0ced3e3`  
		Last Modified: Thu, 16 Oct 2025 20:44:03 GMT  
		Size: 21.2 KB (21206 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc682bac92aeba29afdbced916c30c700365d2d84d67f73c907bbc9ba2e54c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285091605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eaa735d06af5b82dfcdcd7a16c006b70f4f831e4fd9a0b1189c7aeca7b15cb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 07:06:58 GMT
ENV container oci
# Mon, 06 Oct 2025 07:06:58 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Mon, 06 Oct 2025 07:06:58 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 07:06:58 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 07:06:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 07:06:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 07:06:58 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 07:06:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 07:06:58 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV NEO4J_SHA256=670888ac88010ddb09df8a82b3f9f3552f03b16e8197e5855110aac86fe36f35 NEO4J_TARBALL=neo4j-community-5.26.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 06 Oct 2025 07:06:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
# Mon, 06 Oct 2025 07:06:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 07:06:58 GMT
WORKDIR /var/lib/neo4j
# Mon, 06 Oct 2025 07:06:58 GMT
VOLUME [/data /logs]
# Mon, 06 Oct 2025 07:06:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 06 Oct 2025 07:06:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 07:06:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555525045974a3d055c1d413d1442ea340b6f9fd988b1d0459ea711a2fd516b6`  
		Last Modified: Thu, 16 Oct 2025 19:29:11 GMT  
		Size: 124.6 MB (124562647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a424753af885375290813aae21428a2dfb121d193ae322931b22faeddf73030f`  
		Last Modified: Thu, 16 Oct 2025 19:28:49 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a43a0635444453e0ea900b575e0f51557eb27a80160aac9726d13a914cd7aa2`  
		Last Modified: Thu, 16 Oct 2025 19:29:03 GMT  
		Size: 122.6 MB (122622582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3f49422571c22a368c4421417b7ba3db4ebd5738cfa1dd65f15ea53f28ca1f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171e70f57ad485682a274c892efdeb832d8dd80a67fe9edf4080a7273df527ae`

```dockerfile
```

-	Layers:
	-	`sha256:6505b6c9346e77bc4311a7122ef996ba3d445d7b558370acebed931a28da20d6`  
		Last Modified: Thu, 16 Oct 2025 20:44:08 GMT  
		Size: 5.2 MB (5229797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7c46ab0d539bf3d4d02e15055e72132f27e4bf7a62b31d95dd51e21fab22bf`  
		Last Modified: Thu, 16 Oct 2025 20:44:09 GMT  
		Size: 21.3 KB (21341 bytes)  
		MIME: application/vnd.in-toto+json
