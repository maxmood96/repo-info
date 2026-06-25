## `neo4j:5-community-ubi10`

```console
$ docker pull neo4j@sha256:434b7237f2a432c56853b1e9c722db0b1919301d52af69d53d950e117813feef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:d3624e0d147f94d39e17c05c25b9e9cac80918bec3c8c4aebf6bf5e7e231673d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277830733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67e22c283dee7f56d14bd172fad7a72bdc38d61e0e0d9ee7534e54df256c43a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:40:14 GMT
ENV container oci
# Wed, 24 Jun 2026 06:40:14 GMT
COPY dir:92709e786f8e662d73459e8ec6b629a535dce92ae9fcad21b6d7b00ac6803604 in /      
# Wed, 24 Jun 2026 06:40:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:40:14 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:40:14 GMT
COPY dir:e8e2b7cb869a17d32d7452a63fca2737847da7b62b5d0406fabbac5267964ccc in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:40:15 GMT
COPY dir:e8e2b7cb869a17d32d7452a63fca2737847da7b62b5d0406fabbac5267964ccc in /root/buildinfo/      
# Wed, 24 Jun 2026 06:40:15 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:39:51Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:39:51Z" "architecture"="x86_64" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:39:51Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:06:26 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:06:26 GMT
ENV NEO4J_SHA256=5e752081e2863febf3d2f11fab31e1a3185e1ea7bb5e0bcf7d8e516ddbec5349 NEO4J_TARBALL=neo4j-community-5.26.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 23:06:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
# Wed, 24 Jun 2026 23:06:26 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 23:06:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 24 Jun 2026 23:06:29 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:06:29 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 23:06:29 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 23:06:29 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 23:06:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:06:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d16bd660d5aff2d8cb434aefeedc41e2a96fcbfce0e10b612181d05ae773b985`  
		Last Modified: Wed, 24 Jun 2026 09:11:20 GMT  
		Size: 34.9 MB (34866797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae1690d2aef83e0eeb3e247384e390d8b55c947fa078c4ff1ec81a74b6666c0`  
		Last Modified: Wed, 24 Jun 2026 23:06:49 GMT  
		Size: 86.2 MB (86224022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f88e7669375b78e34c3276a0727dd15054edf33c078227f24d00419c945cf6`  
		Last Modified: Wed, 24 Jun 2026 23:06:45 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881140d34ab63e2caac548f53e722f3580bc61e8aaa1fcc553f9eb53e2131f31`  
		Last Modified: Wed, 24 Jun 2026 23:06:50 GMT  
		Size: 156.7 MB (156729820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:1825741065f67e2bc9947a72cea2a9cd738a8aca5f2da9315caa1a56e7a8f656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1634486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd08d6152e946614d7dd22ec9f57b3a196ea7533ab2f6e05e80d5f648c77ee2b`

```dockerfile
```

-	Layers:
	-	`sha256:c6d46fa43421737cb359ad5e28448312990c3c95e9d49ba6caf1f8534190d7ff`  
		Last Modified: Wed, 24 Jun 2026 23:06:45 GMT  
		Size: 1.6 MB (1613537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb711f0b0f2883daec28cbf9bd63da368995b805fed1fc6e1832f68e8fe29603`  
		Last Modified: Wed, 24 Jun 2026 23:06:45 GMT  
		Size: 20.9 KB (20949 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9a4fc5be06d2c157e2d1fafba07fbfdf9cfd1092692f7cb2f595252e183aeb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274954519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c727aae9adb5b1b2f75c2303e0138f7060c622829a6d2145bd38d8d561bbf3ee`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:45:18 GMT
ENV container oci
# Wed, 24 Jun 2026 06:45:18 GMT
COPY dir:0b29f9e66bf048f7202a79e2f728b8f136d2a972d39ff75508b0f9653d433ed0 in /      
# Wed, 24 Jun 2026 06:45:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:45:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:45:19 GMT
COPY dir:1852be49c9caac8615951d68388d7f8791140b539cc11bfda91b044119d75a5d in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:45:19 GMT
COPY dir:1852be49c9caac8615951d68388d7f8791140b539cc11bfda91b044119d75a5d in /root/buildinfo/      
# Wed, 24 Jun 2026 06:45:19 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:44:57Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:44:57Z" "architecture"="aarch64" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:44:57Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:05:49 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:05:49 GMT
ENV NEO4J_SHA256=5e752081e2863febf3d2f11fab31e1a3185e1ea7bb5e0bcf7d8e516ddbec5349 NEO4J_TARBALL=neo4j-community-5.26.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 23:05:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
# Wed, 24 Jun 2026 23:05:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 23:05:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 24 Jun 2026 23:05:52 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:05:52 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 23:05:52 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 23:05:52 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 23:05:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:05:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6bcf33c78aa091990500f016c1ed0cb35bc3f67461b918afc9de35f0b601382c`  
		Last Modified: Wed, 24 Jun 2026 09:11:21 GMT  
		Size: 33.0 MB (33046417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2984e91105ac9bda0b6cabd148fbb416bf267e7c3fd83206df1540667e56eaf5`  
		Last Modified: Wed, 24 Jun 2026 23:06:11 GMT  
		Size: 85.2 MB (85168238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ffc6d1985e40b56b3c8f2ff490bd242d61e3ec1e0e0f9bef74b57cd67bc382`  
		Last Modified: Wed, 24 Jun 2026 23:06:08 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9900dda88442febe8753a2d1699b9ce11b397743f873f173144917b566b0de6f`  
		Last Modified: Wed, 24 Jun 2026 23:06:12 GMT  
		Size: 156.7 MB (156729770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:75e4c3473e3c382d764501628da08a969462b3a2284f5809f2288faad190d74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1633906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e2c5f2e852e1f28d404e13edfd515b491cba45ef423d8cab2f3fd493dc7b69`

```dockerfile
```

-	Layers:
	-	`sha256:b107de8ab97a6a9bd9bd761a2174ec54229d69c5f7a7c133fa76ef9982c38a8c`  
		Last Modified: Wed, 24 Jun 2026 23:06:08 GMT  
		Size: 1.6 MB (1612820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7084a963bdffa6f67a3e4468ab2dfd6459c75b3645675a129c9ebbceb4c3993`  
		Last Modified: Wed, 24 Jun 2026 23:06:08 GMT  
		Size: 21.1 KB (21086 bytes)  
		MIME: application/vnd.in-toto+json
