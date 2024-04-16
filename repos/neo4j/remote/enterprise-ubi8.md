## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:523da04327eb338b4a881916cda13dc26f870b0a4a07184ceb1e3687db662405
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
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
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
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
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json
