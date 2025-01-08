## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Wed, 08 Jan 2025 05:47:29 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json
