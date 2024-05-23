## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:51dfb161abbb7b276378dfef1abd0b8d65b6db2b7a57c55f1880d6de704ae689
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:4d39251fadd67a300340a426730dd1a1cf2b8ec9114340e264f91ef2550f287a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326730915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40407ae1650e61d66493b382f5efa144335ce86d9e070ff5093ff4467e4298fc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:1e33171104997f0a23d074b9a14db4a4771951c35437300603bf95dc6e59cb86 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=896
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:a9412abf195f6cf63b75397952b33f829a9372edd9dd4effce36817f4f80f248 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:3b0ec9f0d37da7a6f59430134740c3967cbd97a86ad4dcfb8850cecebafe2129 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9d49001ad6c59e36fff8fa74763be0954414b6ad5333f7855bb70fa0d6e86cb6`  
		Last Modified: Wed, 22 May 2024 13:49:28 GMT  
		Size: 39.4 MB (39378105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de78290384b37d716c1255063813dd090f2ab490bab6678af817ecbab49b17ce`  
		Last Modified: Wed, 22 May 2024 23:55:55 GMT  
		Size: 164.5 MB (164515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cbb9221218c59540e83a72b4461f718ef460d3678a90f6eb8806e07a09f41f`  
		Last Modified: Wed, 22 May 2024 23:55:52 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024d95c888eb1f82dba373341cb7bb76c9e451d0dbae64d646821099eacbf876`  
		Last Modified: Wed, 22 May 2024 23:55:54 GMT  
		Size: 122.8 MB (122827213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5a51f728f4ce812a5e013ba8e2de7f64b062e1bd7646a737bb01c2261e778fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2895b3f139dcd3d33ac52bacfb0ceadb8cbe6098b62fd62441e3083ba6916071`

```dockerfile
```

-	Layers:
	-	`sha256:bc43a554b85c2e2d102a8305e8601e0cd94533e3ccbd6787546446a1b58ead7b`  
		Last Modified: Wed, 22 May 2024 23:55:52 GMT  
		Size: 10.8 MB (10835368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e5f61701938cd0ef4b4440dc88106e34824391aed16fc0448ebeb10b3b2636`  
		Last Modified: Wed, 22 May 2024 23:55:52 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ad01ecc549694ae1800295f98ca01d300cf899a391fd9425ead14f5ae4ee3c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323514987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834ae558d59d1aad1bf9df3e638d27783756753fca24707a5e7b011e43723037`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.expose-services=""
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL io.openshift.tags="minimal rhel8"
# Fri, 12 Apr 2024 11:14:18 GMT
ENV container oci
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -rf /var/log/*
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL release=896
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bbb36620d7075637d427abcbba06cd2b4020cff7b8398149376edfb815fc11`  
		Last Modified: Thu, 23 May 2024 07:36:16 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82aef2c361c8fc9bc69775fa5d8ce1bbebeea517136933f76daee5d7daec656`  
		Last Modified: Thu, 23 May 2024 07:36:19 GMT  
		Size: 122.8 MB (122827244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6d53fb094134fcd7efc006fa7aa8e590f579741b72d9604ff1b32c18d05bf815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10854571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f55b319c8817e7f654c2d2fc9f4bb757595580812a8cd1f5ef83608265f973`

```dockerfile
```

-	Layers:
	-	`sha256:8d88c7eaebaa7c77102e1e70623907f486ceb639d26cbc421ff314b4f1fa7d90`  
		Last Modified: Thu, 23 May 2024 07:36:17 GMT  
		Size: 10.8 MB (10832914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a456e2f664467a3a721ed8303aed87f8f10e877efdd2f70984b2b095a7cf19ee`  
		Last Modified: Thu, 23 May 2024 07:36:16 GMT  
		Size: 21.7 KB (21657 bytes)  
		MIME: application/vnd.in-toto+json
