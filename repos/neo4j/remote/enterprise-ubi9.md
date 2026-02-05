## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:63886ff77e3fc7dae26c3ca3ea6328a863ebdf6f8b62c5a2b261d83dbce218f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:5c4d5bfe5e2f1309e5f049d6884f7420c803da29dcea90e4d0a9be73da82788a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.9 MB (528938649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d996ac202e733ae18b2d8ef18296e60fed8d3438ac79bf5d068c0fee237873fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:11:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:11:40 GMT
ENV NEO4J_SHA256=3326a905d4accc1bdd224923a6d30c9a498bbd0fb7b43e87983aec29734c367d NEO4J_TARBALL=neo4j-enterprise-2026.01.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 05 Feb 2026 00:11:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
# Thu, 05 Feb 2026 00:11:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 05 Feb 2026 00:11:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 05 Feb 2026 00:11:47 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:11:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 05 Feb 2026 00:11:47 GMT
VOLUME [/data /logs]
# Thu, 05 Feb 2026 00:11:47 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 05 Feb 2026 00:11:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:11:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539d6c7bade4c19ffc55b230ddf37a795fa03e154b8bd5d7dddaea23241aa347`  
		Last Modified: Thu, 05 Feb 2026 00:12:19 GMT  
		Size: 131.6 MB (131601241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ece8cab097de6f02b944c6b39f95d7600d9777a292499ba47c3e282f5821c3f`  
		Last Modified: Thu, 05 Feb 2026 00:12:13 GMT  
		Size: 10.2 KB (10179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f792aa6c4a923c0fbae230ec9aedb3985cc7c1e0c2640ec2c7ff0f0140ceb3`  
		Last Modified: Thu, 05 Feb 2026 00:12:23 GMT  
		Size: 357.3 MB (357318138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:441d508a065606cd3a374263fe843b4e436d4a524194077231c62c61bead5b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5653873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1de042955afc4fe43a5302913e669aef9127ce2b4d0637edb21edf896d14cb5`

```dockerfile
```

-	Layers:
	-	`sha256:d1ceed18ff55a413329dc09126f60008c2aa0826522d906603f37700ca62998e`  
		Last Modified: Thu, 05 Feb 2026 00:12:13 GMT  
		Size: 5.6 MB (5633256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:631bf185ee4480c0adcae9ab6e44063c3733d77a0acc2739b8b87e611c923be8`  
		Last Modified: Thu, 05 Feb 2026 00:12:13 GMT  
		Size: 20.6 KB (20617 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b5be017cc06728c80987ce2c6af9a334644d6e01219a165c9080b7ed4ba024c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.8 MB (526770624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d189709bef4a19610f1164fff97b5f41d1ddd2f2ff7a63e1de3315cc87c396c6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:10:45 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:10:45 GMT
ENV NEO4J_SHA256=3326a905d4accc1bdd224923a6d30c9a498bbd0fb7b43e87983aec29734c367d NEO4J_TARBALL=neo4j-enterprise-2026.01.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 05 Feb 2026 00:10:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
# Thu, 05 Feb 2026 00:10:45 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 05 Feb 2026 00:10:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 05 Feb 2026 00:10:52 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:10:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 05 Feb 2026 00:10:52 GMT
VOLUME [/data /logs]
# Thu, 05 Feb 2026 00:10:52 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 05 Feb 2026 00:10:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:10:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03653459389c4612f26b92ab324712b5875e8b1a10e78d53bdc5df22662b01a2`  
		Last Modified: Thu, 05 Feb 2026 00:11:25 GMT  
		Size: 131.2 MB (131246489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4357c039e9e6eb4742e37802a7bb40a8189ada6333e4e5c5fb43eb00b7644e1d`  
		Last Modified: Thu, 05 Feb 2026 00:11:20 GMT  
		Size: 10.2 KB (10185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089c211cb7cefd889c15b69a791fc3beec2a0df971818a40805de50fefc3d071`  
		Last Modified: Thu, 05 Feb 2026 00:11:29 GMT  
		Size: 357.3 MB (357318197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4b7de4ef3e62d264afb7cbed1de3a1c0c5f50b64358a9618989ebcc89b8faad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5633719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba27f508eba1bc985fff87af0da1cfc5362682307c5745ce938c25a0da702bf5`

```dockerfile
```

-	Layers:
	-	`sha256:a642a31d142f8749cee1c0c18816ad02ed5f930271cb09688c4f3cdb40f7ad51`  
		Last Modified: Thu, 05 Feb 2026 00:11:20 GMT  
		Size: 5.6 MB (5612989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c3a58861d85f92c00dad6778f664d90f642f298b7497714c2d4959ddd0f101a`  
		Last Modified: Thu, 05 Feb 2026 00:11:20 GMT  
		Size: 20.7 KB (20730 bytes)  
		MIME: application/vnd.in-toto+json
