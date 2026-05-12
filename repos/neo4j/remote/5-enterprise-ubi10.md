## `neo4j:5-enterprise-ubi10`

```console
$ docker pull neo4j@sha256:6beb7ebd9dc25dcf597500efe0504ad6925c91f7fb2d8e2b177ef685e04c0a52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:91ee740c911e1bddc422171ccc5135875d7e28bd7f50a755e6927f28d83fcd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616914737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf25321cd860ce3d007a205027ed7ebfb5fdaddb083da4006d6d2dd38ed3cef`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 May 2026 01:16:15 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:16:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:16:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:16:15 GMT
ENV container oci
# Mon, 11 May 2026 01:16:15 GMT
COPY dir:944b21b5e56ba1540a32a325c037508b8301ec37c6f3e20f96a07c3b3ab330c2 in /      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:16:16 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:16:01Z" "org.opencontainers.image.created"="2026-05-11T01:16:01Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:16:01Z
# Tue, 12 May 2026 00:08:57 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:08:57 GMT
ENV NEO4J_SHA256=e417825ffda8b405de7bb7b45788d3810ff270fbe09b7ddc12fb2a6a09de737d NEO4J_TARBALL=neo4j-enterprise-5.26.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 12 May 2026 00:08:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
# Tue, 12 May 2026 00:08:57 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 12 May 2026 00:09:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 12 May 2026 00:09:06 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:09:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 12 May 2026 00:09:06 GMT
VOLUME [/data /logs]
# Tue, 12 May 2026 00:09:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 12 May 2026 00:09:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 12 May 2026 00:09:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:288c81655277add7fa3f1d2c80956ecdc30e861ea53ff003f0eb7d1f488bf24b`  
		Last Modified: Mon, 11 May 2026 02:07:21 GMT  
		Size: 34.6 MB (34622430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2fbc599e09875c3d372a0f497c5a8c264c28a7c07cf4882d1d7df024c48e16`  
		Last Modified: Tue, 12 May 2026 00:09:34 GMT  
		Size: 86.0 MB (86034256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63094f3d32822ef308a4daa43f73057274f628707c5293f486ee01c235195887`  
		Last Modified: Tue, 12 May 2026 00:09:30 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc7d60258dfde222c4d71e4d89d056ccf99e191b1e2b716ac380624bdbdf7dd`  
		Last Modified: Tue, 12 May 2026 00:09:40 GMT  
		Size: 496.2 MB (496247958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:175de0372122c2462eec3ea8320713aaf4ecd9bca4c1c5707d13182f059c3ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1993585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77abc6959f21f724bec1893d7d95c2eb8889d78cef23816d167c7a798d3830`

```dockerfile
```

-	Layers:
	-	`sha256:d63f32de6aeb2a43901c5c960e6b0b890da33d351ca06cb7a1a9f6253d7e8868`  
		Last Modified: Tue, 12 May 2026 00:09:30 GMT  
		Size: 2.0 MB (1973532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9083e0bac540ab3b749aad76aa6a5395c7c361128bb85e82c8007940742a87c`  
		Last Modified: Tue, 12 May 2026 00:09:30 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1272ae844532f1ca41fc18db9ef3c1b8a2a4fd2680427e609d9a0baa9f04963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.0 MB (613984862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f7330fb5f51db74cb773b959a69c8b3751db905150f51e413486aed7d8a965`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 May 2026 01:17:49 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:17:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:17:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:17:49 GMT
ENV container oci
# Mon, 11 May 2026 01:17:50 GMT
COPY dir:c6e5c961b244885bbae5433f1eb0e567eb7e34fa66cb14c7f643fbc5449440ea in /      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:17:50 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:51 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:17:34Z" "org.opencontainers.image.created"="2026-05-11T01:17:34Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:17:34Z
# Tue, 12 May 2026 00:08:44 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:08:44 GMT
ENV NEO4J_SHA256=e417825ffda8b405de7bb7b45788d3810ff270fbe09b7ddc12fb2a6a09de737d NEO4J_TARBALL=neo4j-enterprise-5.26.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 12 May 2026 00:08:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
# Tue, 12 May 2026 00:08:44 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 12 May 2026 00:08:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 12 May 2026 00:08:53 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:08:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 12 May 2026 00:08:54 GMT
VOLUME [/data /logs]
# Tue, 12 May 2026 00:08:54 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 12 May 2026 00:08:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 12 May 2026 00:08:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b0d48ca6ae597735e3215ce3085802fb19010a7e5256d1d09af0257d955c5185`  
		Last Modified: Mon, 11 May 2026 02:10:59 GMT  
		Size: 32.7 MB (32747172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ea6663327c240c1d1192d63a36e955640ad83c8f638683d2ba44cf7c7cd872`  
		Last Modified: Tue, 12 May 2026 00:09:25 GMT  
		Size: 85.0 MB (84979685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d5bfc3ff6649aa2f77f25a2588e9609b51b044da06023be1b68b8df6429fe`  
		Last Modified: Tue, 12 May 2026 00:09:22 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8095f95fb732131cf8809456b1fe83880be5aeb983c3c100ea1e0701b1aa89dc`  
		Last Modified: Tue, 12 May 2026 00:09:32 GMT  
		Size: 496.2 MB (496247911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:30746139ae2624563c822dc65b0ff79c9ba483d26d92ba17929f1fabfbb16657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1992933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0a461b7db3a69058c9dfc2f3c13a574730369e4cf789692972b59bf81ae98a`

```dockerfile
```

-	Layers:
	-	`sha256:5d944dbc2a58dc63be57edbbafebe72e8332c5a664901e2dca9639ed24c09e32`  
		Last Modified: Tue, 12 May 2026 00:09:22 GMT  
		Size: 2.0 MB (1972779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5821e5e08ca8564df1c1d8af2c46f867a252e1cf610be03de4da8dc16758fc2d`  
		Last Modified: Tue, 12 May 2026 00:09:22 GMT  
		Size: 20.2 KB (20154 bytes)  
		MIME: application/vnd.in-toto+json
