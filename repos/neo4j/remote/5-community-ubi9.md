## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:97a550fd818e65130862fe8eeb5bea37967a73ba2678c8c7fd6aca3548702c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:91e40b035f1876ef7fcc331704689ef4f65f6abfc53fd1864b62618c2ce4888c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321753857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ea429d8054fb4c118f256157c16c7c6716bf13bc8ff6b69954b713dc7b7815`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 May 2025 09:58:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 06 May 2025 09:58:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 06 May 2025 09:58:59 GMT
LABEL url="https://www.redhat.com"
# Tue, 06 May 2025 09:58:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 06 May 2025 09:58:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 06 May 2025 09:58:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 06 May 2025 09:58:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 06 May 2025 09:58:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 06 May 2025 09:58:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 06 May 2025 09:58:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 06 May 2025 09:58:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 06 May 2025 09:58:59 GMT
ENV container oci
# Tue, 06 May 2025 09:58:59 GMT
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Tue, 06 May 2025 09:58:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 06 May 2025 09:58:59 GMT
CMD ["/bin/bash"]
# Tue, 06 May 2025 09:58:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 06 May 2025 09:58:59 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Tue, 06 May 2025 09:58:59 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 06 May 2025 09:58:59 GMT
ENV NEO4J_SHA256=b5227fa3cf5c94b7da8186ded58dbd1937cad46bec08c7f862cfc402b03ff42f NEO4J_TARBALL=neo4j-community-5.26.6-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 06 May 2025 09:58:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.6-unix.tar.gz
# Tue, 06 May 2025 09:58:59 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 06 May 2025 09:58:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.6-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 06 May 2025 09:58:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 09:58:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 May 2025 09:58:59 GMT
VOLUME [/data /logs]
# Tue, 06 May 2025 09:58:59 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 06 May 2025 09:58:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 May 2025 09:58:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5019d50f4259d6937d3ec0b38cb601fe489455b8ca933695ea361ed91e7460d`  
		Last Modified: Thu, 15 May 2025 20:48:53 GMT  
		Size: 124.4 MB (124422479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c6d57344eb7645a021a049d9140ce39e0a7a1f646dc8b9de02dcfbcd9b5a0f`  
		Last Modified: Thu, 15 May 2025 20:45:48 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1cdfdee1c2581d6e0df742d3841d071ae72ad1d9b4a217a357ffea520bb94`  
		Last Modified: Thu, 15 May 2025 20:48:58 GMT  
		Size: 157.7 MB (157676219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:30d1c994f80197fea5811fd5edb0e9c395d21d3c222735d47fc531f04266445c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368b0d46af2bcf8b9eaa25bd3d70dfd9215324be6f71273cd8d2e288cc9de243`

```dockerfile
```

-	Layers:
	-	`sha256:dafb184d9cd163bdb5e62456c04bdd6afda1140611444ae353cc9a9258ad5d52`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 5.3 MB (5286825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e356b1d47c67f9f439bc789cc131f82c12917881ef19745fd5fc631d5f95add`  
		Last Modified: Wed, 14 May 2025 23:48:47 GMT  
		Size: 21.2 KB (21163 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2dfe4603dcc3e635737652b0f1741ea44beb6f175c667c359e148932c69b3c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (319954828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0727b7e5e59f5f8ccf3e7084d0fc1641920ab403c69c461361dc1553f761fff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 May 2025 09:58:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 06 May 2025 09:58:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 06 May 2025 09:58:59 GMT
LABEL url="https://www.redhat.com"
# Tue, 06 May 2025 09:58:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 06 May 2025 09:58:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 06 May 2025 09:58:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 06 May 2025 09:58:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 06 May 2025 09:58:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 06 May 2025 09:58:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 06 May 2025 09:58:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 06 May 2025 09:58:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 06 May 2025 09:58:59 GMT
ENV container oci
# Tue, 06 May 2025 09:58:59 GMT
COPY dir:3fa6b42aa9cb1575a22397e201df9f16228db85fb99450db2e9f8bef40a52c0f in / 
# Tue, 06 May 2025 09:58:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 06 May 2025 09:58:59 GMT
CMD ["/bin/bash"]
# Tue, 06 May 2025 09:58:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 06 May 2025 09:58:59 GMT
LABEL "build-date"="2025-05-14T10:40:32" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Tue, 06 May 2025 09:58:59 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 06 May 2025 09:58:59 GMT
ENV NEO4J_SHA256=b5227fa3cf5c94b7da8186ded58dbd1937cad46bec08c7f862cfc402b03ff42f NEO4J_TARBALL=neo4j-community-5.26.6-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 06 May 2025 09:58:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.6-unix.tar.gz
# Tue, 06 May 2025 09:58:59 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 06 May 2025 09:58:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.6-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 06 May 2025 09:58:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 09:58:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 May 2025 09:58:59 GMT
VOLUME [/data /logs]
# Tue, 06 May 2025 09:58:59 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 06 May 2025 09:58:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 May 2025 09:58:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9cf99093c2fb01ee3da769d664a9212c42b7d50516f9e77975132a6540ccdf3b`  
		Last Modified: Thu, 15 May 2025 19:25:04 GMT  
		Size: 37.9 MB (37876105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe4cd13530e532fa31e33704f9d484ab9195622f896e7408f1afa28930291be`  
		Last Modified: Thu, 15 May 2025 20:49:47 GMT  
		Size: 124.4 MB (124392392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82c5aa8628e894fed7f0ef9aaedbe1004902ac3714086b3515140ebf654e156`  
		Last Modified: Thu, 15 May 2025 20:49:33 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484c7ca08073314386a62f509bb50aaccb0f6e4ca4b2a6aae779dfefb0a3f7d`  
		Last Modified: Thu, 15 May 2025 20:49:46 GMT  
		Size: 157.7 MB (157676271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:42e0f5a0cc7fa11ce3e0df301c967a9319a6823b5eadb77360a820e5bd9ac746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96461d68ea2702bc7abf9f264ed4cbe3c24bc9f2d9ca276f73e36fc6f396f90a`

```dockerfile
```

-	Layers:
	-	`sha256:617cf876ec0e31e3899357388cdfa3a66eda5d8ac20006172cc3c4a57711622f`  
		Last Modified: Thu, 15 May 2025 00:11:10 GMT  
		Size: 5.3 MB (5266591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda1332e101efe2c848f3c1fe590f44b3f98ab917be09271426675103202944a`  
		Last Modified: Thu, 15 May 2025 00:11:09 GMT  
		Size: 21.3 KB (21298 bytes)  
		MIME: application/vnd.in-toto+json
