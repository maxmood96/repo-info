## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:eb67c5141f544cc3beb967a109ab44484ec2a99c876a23e1ebbbb34b93f8b0f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab39147e55f860c01e06aadb376e28d88a1d064fb771baeca25b6fd53cc7ab55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315476088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1eafda468793c069679d1a42b7d205852af596fc8fc67c50e401c8596aff94`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:04b5206f5aaacde0180f109fb607ee5fc401f9df5c5428b84c16533af7850fb0 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:49e32581c248adb5f2489c4689550d8d7a9e1940bfbc1e91bc5b576efcad75f6 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d1fb41b6521c101e62eef237a92f0fb92dde0b380363a4f5901d3b4dc45104e8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:486b0fdd7ff16122ace0252fbf127e70ece0dfaa405eaac4b617260c0d41a919`  
		Last Modified: Tue, 28 May 2024 15:06:03 GMT  
		Size: 37.7 MB (37668361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b3f46071245444225f0923ac16323be786e0d94feb3206e7fd22d84c14e387`  
		Last Modified: Thu, 30 May 2024 12:42:38 GMT  
		Size: 151.4 MB (151360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c728118b9380fb212a34583b8bde76d04ae6e47eda5d8d7d3e416b0e9db3bf1`  
		Last Modified: Thu, 30 May 2024 12:42:33 GMT  
		Size: 9.7 KB (9727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d901aeabea182fdab86f9207cdecc6ce7c74eaa1eff3e48a0b3a61a6a6c369dc`  
		Last Modified: Thu, 30 May 2024 12:42:36 GMT  
		Size: 126.4 MB (126437799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7956a20615949ebbf9cc45e347ebd887c644d393dba415e79bb045eb82f62f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bae9c2185bfeb3bae2e85bd54c9f87d734dbe46abc95245c03878dfdcdf56ce`

```dockerfile
```

-	Layers:
	-	`sha256:417c896824d31ae12583fcb6cacdde48c16ebb11e088ccc5824370393c39c6a3`  
		Last Modified: Thu, 30 May 2024 12:42:33 GMT  
		Size: 10.3 MB (10307461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42f20433a8f1a32ff717656f8948bb3d65d7bdd88fe4a40e8e4de18cb7f9caa2`  
		Last Modified: Thu, 30 May 2024 12:42:32 GMT  
		Size: 21.8 KB (21828 bytes)  
		MIME: application/vnd.in-toto+json
