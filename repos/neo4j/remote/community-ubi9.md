## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:70852b2ab996bf8f4ee0a5f7e679bb1f4e1be0d5cb6e92a901bb029620f3677b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f57e710e50f6f6cad8f7c8848ecdbd2596499b4a3833ea670c1168c7755cd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331068087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffc87b00658ddef9d2e1ddda258be139bffd39a6ab2ce03dd7b98dc6f2ebf68`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL url="https://www.redhat.com"
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL io.openshift.expose-services=""
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 29 Apr 2025 10:30:01 GMT
ENV container oci
# Tue, 29 Apr 2025 10:30:01 GMT
COPY dir:2dc25289c3b10f6fae681d085452474bf4d133d8f435510e0e9aa64114b861ab in / 
# Tue, 29 Apr 2025 10:30:01 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 29 Apr 2025 10:30:01 GMT
CMD ["/bin/bash"]
# Tue, 29 Apr 2025 10:30:01 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 29 Apr 2025 10:30:01 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL "build-date"="2025-05-13T04:42:10" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7575d7eb45eb7f545fef31ba067dfe3d8e52c4eb" "release"="1747111267"
# Tue, 29 Apr 2025 10:30:01 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV NEO4J_SHA256=118cb439904d1aaad67f2421be518d2acc2b754f621acc209ee3362e5b67ba65 NEO4J_TARBALL=neo4j-community-2025.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 29 Apr 2025 10:30:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.04.0-unix.tar.gz
# Tue, 29 Apr 2025 10:30:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.04.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Apr 2025 10:30:01 GMT
WORKDIR /var/lib/neo4j
# Tue, 29 Apr 2025 10:30:01 GMT
VOLUME [/data /logs]
# Tue, 29 Apr 2025 10:30:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 29 Apr 2025 10:30:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 29 Apr 2025 10:30:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:719fed365262e942a8d13a9f7c6f9e87e6274c4e3ad3d0efc81666b12229084d`  
		Last Modified: Tue, 13 May 2025 05:25:18 GMT  
		Size: 39.7 MB (39714170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddc9b605de02a162705fe8a6a84f7b1c9fe61945b65b4876d990b0a0c28c2d3`  
		Last Modified: Tue, 13 May 2025 19:54:53 GMT  
		Size: 132.4 MB (132434650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163c76fa39111251adf5b223efde6e6580182dac5768d9b1ba59fe50f75931a2`  
		Last Modified: Tue, 13 May 2025 19:54:51 GMT  
		Size: 10.0 KB (10025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf627deaf3b384dbc914f836af08567ba9975014f0ec634e1542df69818eb4c`  
		Last Modified: Tue, 13 May 2025 19:54:54 GMT  
		Size: 158.9 MB (158909210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a4f73dc68f8d004d06b8c98b574fa7810849bcb6763b41f68fdaf0d25f65e169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92362e4365a262b703948e631ddb3f6f097e2e7c94a5d6e8c0246869147643a7`

```dockerfile
```

-	Layers:
	-	`sha256:bc45c68a5a67d2709a3a8233e2645df8a6e4fc225b74d47831583faf499f6894`  
		Last Modified: Tue, 13 May 2025 19:54:51 GMT  
		Size: 5.3 MB (5345784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44efff778bc695da40f6aa7e1bb516386d9aec95a1f8b557d7a829b5637c6ebe`  
		Last Modified: Tue, 13 May 2025 19:54:51 GMT  
		Size: 21.8 KB (21826 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d4666a22cd5c6755d7fca5d6b96b4e893f0a8d6300543b0fb913d68c502d4c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328551701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ef578cd8ef8e7215a3261f8543336cbbc93dce7ab93224f565672415c528e9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL url="https://www.redhat.com"
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL io.openshift.expose-services=""
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 29 Apr 2025 10:30:01 GMT
ENV container oci
# Tue, 29 Apr 2025 10:30:01 GMT
COPY dir:322b1eba0279fa9048b9b4a366e8c52ac2af46fb06d006174f85e5f3b1ca4d6a in / 
# Tue, 29 Apr 2025 10:30:01 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 29 Apr 2025 10:30:01 GMT
CMD ["/bin/bash"]
# Tue, 29 Apr 2025 10:30:01 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 29 Apr 2025 10:30:01 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 29 Apr 2025 10:30:01 GMT
LABEL "build-date"="2025-05-13T04:46:37" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7575d7eb45eb7f545fef31ba067dfe3d8e52c4eb" "release"="1747111267"
# Tue, 29 Apr 2025 10:30:01 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV NEO4J_SHA256=118cb439904d1aaad67f2421be518d2acc2b754f621acc209ee3362e5b67ba65 NEO4J_TARBALL=neo4j-community-2025.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 29 Apr 2025 10:30:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.04.0-unix.tar.gz
# Tue, 29 Apr 2025 10:30:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.04.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Apr 2025 10:30:01 GMT
WORKDIR /var/lib/neo4j
# Tue, 29 Apr 2025 10:30:01 GMT
VOLUME [/data /logs]
# Tue, 29 Apr 2025 10:30:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 29 Apr 2025 10:30:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 29 Apr 2025 10:30:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3a51516451292e212d18ae92028ed74f1d747fc2bc7752aa8c608a2cc7d626cc`  
		Last Modified: Tue, 13 May 2025 05:30:51 GMT  
		Size: 37.9 MB (37887912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba126affc4828ae96cc1249028395a3229aac4483ade4047c4d33fbbb969c2e3`  
		Last Modified: Tue, 13 May 2025 20:15:54 GMT  
		Size: 131.7 MB (131744531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f2ec5ce75bbdce53df64721915942d5ec877d70542a73702d6b084e3bd1476`  
		Last Modified: Tue, 13 May 2025 20:15:51 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47acf7e4176ef0a8b62d7eb2b8799a84887f54176c88f8781a9331989c2744e1`  
		Last Modified: Tue, 13 May 2025 20:15:55 GMT  
		Size: 158.9 MB (158909202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:973a9af374b9f68533aafc9ff73ce40d0d058e990595c59d6c1606444e237f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618788606a3150dccace0f22e57dfac00d29290868dd68e880bf371beca0a087`

```dockerfile
```

-	Layers:
	-	`sha256:c720e76adb7cf41949b98fd519560e8259afa640cf03a13bec95d3b13270ea46`  
		Last Modified: Tue, 13 May 2025 20:15:52 GMT  
		Size: 5.3 MB (5325222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcbe756ae05efd7f2036c06f9f57757428aabeb7bd06d303c1ae0283fb85c0a9`  
		Last Modified: Tue, 13 May 2025 20:15:51 GMT  
		Size: 22.0 KB (21987 bytes)  
		MIME: application/vnd.in-toto+json
