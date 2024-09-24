## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:d2e683c67f2d0b980da98856ace472e503312f04d16f8800101959402471e88d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8b26beb7abd1542bf5757c65f93161ea9079056dfb77b756af298e3dc639a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288892373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4196fc6aa925c5bc6200c4cbbc63f0731faf6e7067e1e784ab2291b088660e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140bcfdd5280378a532acc9f4a2403323c1b5e5cca567235b36c23ae18b969f`  
		Last Modified: Wed, 11 Sep 2024 02:02:40 GMT  
		Size: 125.5 MB (125451611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc67fd62f489e54607a918a4dd2a1e2a4af4aa14b094746628598b510e034f`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf411414e97963d53b5c9421d2331d80b88b20b77505ce408fd307a32d89073`  
		Last Modified: Wed, 11 Sep 2024 02:02:39 GMT  
		Size: 124.3 MB (124348641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e1b7083880317b63bf3a082672d6c8f8fdf08c0ffc0bc0e8b0538bda279fbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3ac334b693a06a2f58b46e663c16683e5cfb3c6854400a49ed1c72c588be1`

```dockerfile
```

-	Layers:
	-	`sha256:28f5cc94b1ee47452323595aa3c1d1847eea6c063c47a41797bb9e5dcc7dc8c6`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 5.3 MB (5256785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea667173e1fe09b8908999f9c4d07f82a137f3403aafabcd05b54c7f36f3f83`  
		Last Modified: Wed, 11 Sep 2024 02:02:37 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b434eff505440dcc5f1300b7d9593b92bede39ddf5671c45957c149f377b284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287152268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100909fbb1b910412e47364cdd30cdc03111552e43af49fc93b1b95b20098a0c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3b708771449b1058f44f70932e1fa3868e1876107200b42fa17ab54d8ac089`  
		Last Modified: Tue, 24 Sep 2024 01:12:58 GMT  
		Size: 125.5 MB (125458540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d44a2f712becd634bcbe851a9ebdf018848d6c2e32bf8b2b0ba37b7c95cff`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aa237c5a48019c4e9f67746ca7c30e2980798b04e4277c2d5ba80c70db7b9`  
		Last Modified: Tue, 24 Sep 2024 01:12:59 GMT  
		Size: 124.3 MB (124348656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:cf28fc857e6f49c6f7093163c5c3213d8c223c802a65431b92a7bd21ea95deb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd1ba6e0ec09093d45a1034696b3986742ef28383629290966b124d58efb73`

```dockerfile
```

-	Layers:
	-	`sha256:c9b24924c6f572004d9933f2d27a0a279594cea367b25b993f6e9adc5338a6a3`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 5.2 MB (5236424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9ffcfef31d3564087854428f3f9bbd7bf021fc5ed241f9164419d84f66dc54`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json
