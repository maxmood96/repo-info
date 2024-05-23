## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:b01ba9636f5f4a0bd66889f8a5c4c6e4fcc776d3e374ffa953fc35d2222e53a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

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

### `neo4j:community-ubi8` - unknown; unknown

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

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3011454bf07fffaca58ee6e70cbbb3d53438c582eae5c34cda5f50066f7ab427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311472717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c373ac79ed40c9f036d4fc8d4bd8efb52f65e86399a8cd8b0c22d7d7eba4e8f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:b61c459fab0c831bd20d2edec8656e6a48d14508bac1b88a475be015ed609be1 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD multi:e7823a6c139bf1ba69d88420a6fdb05c6cf16ced7a36a870a692d325eaaeb432 in /etc/yum.repos.d/ 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
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
ADD file:249d8e86d28ee6ccadc1e94aafb611d7e259a3c8de906252aa690bf0cbe544e7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.1715068733.json 
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:6e0d7ea605f1760b3b01692bf1473ee5ec8196aa92bec59b7407f178adf4d59a in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161.1715068733 
# Fri, 12 Apr 2024 11:14:18 GMT
LABEL "release"="1161.1715068733" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-07T07:59:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161.1715068733"
# Fri, 12 Apr 2024 11:14:18 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3043758-2f9bd.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
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
	-	`sha256:b70cdb37098f86a1ccd1a09b3b94f2610ea0539ce08dfa5fabcc53dcb3bf76d2`  
		Last Modified: Wed, 08 May 2024 18:29:40 GMT  
		Size: 37.7 MB (37737169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af13b2607b7a68577302e0d19d9caeac4444c198f8b8e00beeb16ed42a49b160`  
		Last Modified: Fri, 10 May 2024 19:15:14 GMT  
		Size: 150.9 MB (150898624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed598b19a4f66b31787d7a0b24efd6b0fbd483a115a968bd1a9637a47c2161`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ad08967183eccc83a2f31d1411c1b5a6bf0c63abb890830adc14ea8d92b6b5`  
		Last Modified: Fri, 10 May 2024 19:15:13 GMT  
		Size: 122.8 MB (122827195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0146bea84b52b7fd53ae3ca617fe4983fbb7a26a5adc603a61fa73aabc9d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7ddf001be8bfcb61f29efdd2574298142e5ce5b6270676e4d2aaa2522d32c`

```dockerfile
```

-	Layers:
	-	`sha256:30fe0a08b103865074524ad277ad878a505520ccfa95608d3811eb6a573ef009`  
		Last Modified: Fri, 10 May 2024 19:15:11 GMT  
		Size: 10.3 MB (10304387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700f72c7b590ede7d2d0d1a8bdbbcb20a7bed4215f82aca51ff59bdca8c6cc8b`  
		Last Modified: Fri, 10 May 2024 19:15:10 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json
