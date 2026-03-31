## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:4d803e7737d0d72816d593d73d0a0aabb7404a81b25072a8b2c3161585cd9ab2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ed87e546779281090cab21ba6db12028e30e0ab61c133b8edc57e473a2ebd3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 MB (639691324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3dd35bb2fc72eb5a67f91c38236cbc29cab92168fd5e6b05023e148dcac6d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Tue, 31 Mar 2026 17:49:45 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gzip         hostname         java-17-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 31 Mar 2026 17:49:45 GMT
ENV NEO4J_SHA256=0c97832ac9dd7172c2315c58b957c343644d4f50a863951976bb1b25ba291f5a NEO4J_TARBALL=neo4j-enterprise-5.26.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 31 Mar 2026 17:49:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
# Tue, 31 Mar 2026 17:49:45 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 31 Mar 2026 17:49:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 31 Mar 2026 17:49:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2026 17:49:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Mar 2026 17:49:55 GMT
VOLUME [/data /logs]
# Tue, 31 Mar 2026 17:49:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 31 Mar 2026 17:49:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Mar 2026 17:49:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f948a9b80aef36f6fab9a696669caec5c0332299d304ef6b77828c12be34fd0`  
		Last Modified: Tue, 31 Mar 2026 17:50:24 GMT  
		Size: 87.5 MB (87548981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e979c90f2482c9c6b6af3dc73f9b627351cf40ae2decf4ef4389921cf2321d`  
		Last Modified: Tue, 31 Mar 2026 17:50:21 GMT  
		Size: 10.2 KB (10228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a5c8ec927a06c768312381744a729895809823567b36a016eaab7d0e2a854a`  
		Last Modified: Tue, 31 Mar 2026 17:50:32 GMT  
		Size: 512.1 MB (512100964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5a1e68290b16cd69db5cbb951665c049cbc6b811812e3ca81e19ec31d8b1e0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4207957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76615aefd5b5301367e6f705c4d9ac14d89e0465ee35cc0a33025e5da81cd4a`

```dockerfile
```

-	Layers:
	-	`sha256:bcac9f7188e99a173369db5a72c6b709ea5dc07d2648dc28d361bbd9405a6249`  
		Last Modified: Tue, 31 Mar 2026 17:50:21 GMT  
		Size: 4.2 MB (4187966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc8b67039e54c29e22ed3a62ea0a651d1e0da2a26baa5d77a9c4ad6d901f41c`  
		Last Modified: Tue, 31 Mar 2026 17:50:21 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c230553354e71b8b26c4dc3113dcbbffcd096fc8e1c5878bc2b2654bb7597ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 MB (637308141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e74a809e4cf5ccba000d482504b79d6db992f1c21510a9e826d7de128fad877`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Tue, 31 Mar 2026 17:49:43 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gzip         hostname         java-17-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 31 Mar 2026 17:49:43 GMT
ENV NEO4J_SHA256=0c97832ac9dd7172c2315c58b957c343644d4f50a863951976bb1b25ba291f5a NEO4J_TARBALL=neo4j-enterprise-5.26.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 31 Mar 2026 17:49:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
# Tue, 31 Mar 2026 17:49:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 31 Mar 2026 17:49:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 31 Mar 2026 17:49:53 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2026 17:49:53 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Mar 2026 17:49:53 GMT
VOLUME [/data /logs]
# Tue, 31 Mar 2026 17:49:53 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 31 Mar 2026 17:49:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Mar 2026 17:49:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c7f47a42055855eb7c1258b08078aa8cc74b9b442c418e861fe8bff04edd87`  
		Last Modified: Tue, 31 Mar 2026 17:50:29 GMT  
		Size: 87.0 MB (86991909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797b72e9b2c57b582513de41de33ff6cbc02408146db5914d2b9fbf9bf8de984`  
		Last Modified: Tue, 31 Mar 2026 17:50:24 GMT  
		Size: 10.2 KB (10228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4255e60747bc9d8ca2ddf407b550984dcd245b7341836d1d013af106c4fcf1`  
		Last Modified: Tue, 31 Mar 2026 17:50:38 GMT  
		Size: 512.1 MB (512101070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:25a5c5afe0c1bf1eb91622059b3825fa66eda932635e38421c10d2539c7223f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074cceb1c6c2269d0fccea11c653a2395f054e899827a742103ed4517eba4f25`

```dockerfile
```

-	Layers:
	-	`sha256:90aac2518ab2c1a14e881e3a314ca904d4116f7adf01164f44aa9d0bd2d51366`  
		Last Modified: Tue, 31 Mar 2026 17:50:24 GMT  
		Size: 4.2 MB (4185951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b4111c9836566e3f8999de79387b2be0e29724589d198adbbc376e5a19bdea0`  
		Last Modified: Tue, 31 Mar 2026 17:50:24 GMT  
		Size: 20.1 KB (20091 bytes)  
		MIME: application/vnd.in-toto+json
