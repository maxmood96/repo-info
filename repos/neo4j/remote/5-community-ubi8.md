## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:7219ee209cc14485c2a828911b170c4296462e21cab6cb695f5b80b21903dcec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b18725cb3774cac4857d3b448603e4343d4ac33d8c02afcf0a6cffe1a8a09a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304144045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a850797b78167b08481725813f2fcb82e7a5a171660b6d7bfeed06e42e52fe7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Fri, 19 Jan 2024 01:19:16 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 19 Jan 2024 01:19:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Fri, 19 Jan 2024 01:19:16 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Fri, 19 Jan 2024 01:19:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 19 Jan 2024 01:19:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jan 2024 01:19:25 GMT
WORKDIR /var/lib/neo4j
# Fri, 19 Jan 2024 01:19:25 GMT
VOLUME [/data /logs]
# Fri, 19 Jan 2024 01:19:25 GMT
EXPOSE 7473 7474 7687
# Fri, 19 Jan 2024 01:19:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 19 Jan 2024 01:19:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c75323395ffce4e666c1bed4a295d0d73e23f77de86b5bc19ae2dc4ca6c8fd`  
		Last Modified: Fri, 19 Jan 2024 01:20:20 GMT  
		Size: 9.5 KB (9494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4258db338f2b55222d34ca5d01c5cf80d34deb5844fdf7c0a876b2f0227bf5`  
		Last Modified: Fri, 19 Jan 2024 01:20:26 GMT  
		Size: 112.6 MB (112618761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
