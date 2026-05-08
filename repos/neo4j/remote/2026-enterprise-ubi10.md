## `neo4j:2026-enterprise-ubi10`

```console
$ docker pull neo4j@sha256:988a9d22d209a2fa7b7a89e4f3a519ea49ae984bf3201047956f7fb04855ace6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:10beebd545d24c972932017da3527caf2d69e3aa523413ad24a3bfd5abb0f8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.3 MB (516269051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf9a1e597cd29e04723096eb54b7b845b0c3d3fca4a2634d061886d326853ed`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 06 May 2026 09:10:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:10:13 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:10:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:10:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:10:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:10:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:10:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:10:13 GMT
ENV container oci
# Wed, 06 May 2026 09:10:13 GMT
COPY dir:c68dbe05133c31f8fd9f151252a4a29ce3fdd8d44060b74e88191790dd574dbf in /      
# Wed, 06 May 2026 09:10:13 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:10:14 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:10:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:878ce3a57b93d24e6852d17b3cb65931afbc773f95f9596e50dac7b8ef938cc4 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:878ce3a57b93d24e6852d17b3cb65931afbc773f95f9596e50dac7b8ef938cc4 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:14 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:09:57Z" "org.opencontainers.image.created"="2026-05-06T09:09:57Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:09:57Z
# Fri, 08 May 2026 16:23:09 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:23:09 GMT
ENV NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 16:23:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 16:23:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 16:23:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 08 May 2026 16:23:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:23:16 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 16:23:16 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 16:23:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 16:23:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 16:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92d62aafb6a18663d52e4aabc1138a75b2e6994c38e927e9099cb078cc22e6b7`  
		Last Modified: Wed, 06 May 2026 10:14:33 GMT  
		Size: 34.6 MB (34621721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2320a1e60d34e3547422c371e39e79152970ae64c87fb89336781e59d9c87ae7`  
		Last Modified: Fri, 08 May 2026 16:23:43 GMT  
		Size: 100.5 MB (100465973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e268b66703b7f659da94bdd1b43717ba92e3d2085cffc94c6593ec9bb2bbc9ee`  
		Last Modified: Fri, 08 May 2026 16:23:39 GMT  
		Size: 10.0 KB (10017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f91e82c044b4785fbed4734f7d8e9d5fec7bc483999847065c66f90d17d0a8`  
		Last Modified: Fri, 08 May 2026 16:23:48 GMT  
		Size: 381.2 MB (381171308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:86a17696a2214fd00632af38f361b107c8b589d0f81a4ccbdef3b2535e265837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53dd9d9a937b818320dfa60dad3a1d364973b4d53d8cdc597fc74a4de2001f6`

```dockerfile
```

-	Layers:
	-	`sha256:f04d5782c2606fbd6522bb1eeb19f2bc4ca2a421af048924f7ea9d2fee6320b4`  
		Last Modified: Fri, 08 May 2026 16:23:39 GMT  
		Size: 2.0 MB (2035193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b1279a3a1681853e510e2b61d409eb6d346cb7174925a6cef38a529977414a`  
		Last Modified: Fri, 08 May 2026 16:23:39 GMT  
		Size: 20.4 KB (20403 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ecf30d190dab7209fb77921241b14e0740f1cd331ea9d525e51bbdf58664126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513084867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c6b0cb45474c8dd010dbfa604d178a0a489c81ff644427f690f5c08403837a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 06 May 2026 09:13:03 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:13:03 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:13:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:13:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:13:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:13:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:13:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:13:03 GMT
ENV container oci
# Wed, 06 May 2026 09:13:04 GMT
COPY dir:750bbe41da49fc0c3224e4824b23b1c35d4c73f39652b46f248f5dd9cad107de in /      
# Wed, 06 May 2026 09:13:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:13:04 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:13:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:13:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:13:05 GMT
COPY file:2221d5e6d5258b2c2c2c5ff82716a8550cb92905efa9801612122423d38aec35 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:13:05 GMT
COPY file:2221d5e6d5258b2c2c2c5ff82716a8550cb92905efa9801612122423d38aec35 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:13:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:12:48Z" "org.opencontainers.image.created"="2026-05-06T09:12:48Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:12:48Z
# Fri, 08 May 2026 16:23:01 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:23:01 GMT
ENV NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 16:23:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 16:23:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 16:23:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 08 May 2026 16:23:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:23:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 16:23:08 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 16:23:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 16:23:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 16:23:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e82aa3f29d1a9f34361831d6ff7b3f84cfd92ed1421ee638f165e55be85bd238`  
		Last Modified: Wed, 06 May 2026 10:17:34 GMT  
		Size: 32.7 MB (32746638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91c1fd0d0da15464ce41e94daf310a9d7acbac888163bf1125092c1cc256044`  
		Last Modified: Fri, 08 May 2026 16:23:39 GMT  
		Size: 99.2 MB (99156819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ad47eb2a8070d21ddc302e50dd995be964b867db27b0fad00b54c63c43fe68`  
		Last Modified: Fri, 08 May 2026 16:23:34 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86589291708a7baaac3969949f0abca83de693443367fb39d74f8ac99204df98`  
		Last Modified: Fri, 08 May 2026 16:23:48 GMT  
		Size: 381.2 MB (381171358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:26387fdb926a909c482fb8372fbde64d10dcebdd3a829b7f4495473eac44e97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8059d2882fde6b09b360ec331fad77c7610b5c1aa490c5ee197809f72db542`

```dockerfile
```

-	Layers:
	-	`sha256:04b1aa3f93092c866d7c98012037dfbd14845588f3976c83b0a04e890dec7973`  
		Last Modified: Fri, 08 May 2026 16:23:34 GMT  
		Size: 2.0 MB (2034449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b8ad482ac27cf0f95a73a18872c5f46da350395f9f0db18aedaeee01ceae66`  
		Last Modified: Fri, 08 May 2026 16:23:34 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json
