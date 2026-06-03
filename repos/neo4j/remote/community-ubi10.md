## `neo4j:community-ubi10`

```console
$ docker pull neo4j@sha256:f6fc266d81857fdc04f80ed461e1827dde13e2f960612d63114390014b8dc1ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:cef13263a0392ad3b357ea0b7661ff4be0191d7b8fe5e8e10b0512850e6d10a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 MB (373433158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862636d8cf855e31bc53ad937da8cf8306693005d01f5fcab498be1695684acc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:15:58 GMT
ENV container oci
# Tue, 02 Jun 2026 15:15:58 GMT
COPY dir:e8b072881a1b1351c3b2d1bd84c8a6d6b28cb6b00007243c1b82e61134e4db04 in /      
# Tue, 02 Jun 2026 15:15:58 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:15:58 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:5abe2f7df4c217a707574e953fc9f76f54f8de027108bd9480e64819343fa499 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:5abe2f7df4c217a707574e953fc9f76f54f8de027108bd9480e64819343fa499 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:15:59 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:15:44Z" "org.opencontainers.image.created"="2026-06-02T15:15:44Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:15:44Z
# Tue, 02 Jun 2026 22:47:27 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:47:27 GMT
ENV NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 02 Jun 2026 22:47:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Tue, 02 Jun 2026 22:47:27 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 02 Jun 2026 22:47:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 02 Jun 2026 22:47:31 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:47:31 GMT
WORKDIR /var/lib/neo4j
# Tue, 02 Jun 2026 22:47:31 GMT
VOLUME [/data /logs]
# Tue, 02 Jun 2026 22:47:31 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 02 Jun 2026 22:47:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:47:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e4e3984c47d80f8f7813d099ea4505637390207a530acceb3e7426232f7555a`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 34.8 MB (34839018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85cf8b2cd8daa1d8feb0fb09ac6c41c91ac6a6ed8fe9ba11f88b5f53b6579d3`  
		Last Modified: Tue, 02 Jun 2026 22:47:57 GMT  
		Size: 100.6 MB (100628885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeaaee8b65a7e35dba649164ad2ddffd14885d6588e73e1dd9a8ae5e1881132`  
		Last Modified: Tue, 02 Jun 2026 22:47:52 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003d3644a6d1c068b0a20195bea3a4d010330e53ef5501510f493dd065380e80`  
		Last Modified: Tue, 02 Jun 2026 22:47:59 GMT  
		Size: 238.0 MB (237955204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:7a486b05b1dcde15459fb1e482952375abf85f74b432882d79574f45b5410898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1755541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ec55855fd0da8cb04f268edbff07e737f99b9bf424a66e49fd1f5f81137230`

```dockerfile
```

-	Layers:
	-	`sha256:b2406dcf3b034749a355175365698a9efbb122134849061cab847e4b5bf67a05`  
		Last Modified: Tue, 02 Jun 2026 22:47:53 GMT  
		Size: 1.7 MB (1733934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f77534e99e148a82947ed5fb5a8f57024f7ee12f1c102a3651b536d50f866ca0`  
		Last Modified: Tue, 02 Jun 2026 22:47:53 GMT  
		Size: 21.6 KB (21607 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c7c882599e18c680abb7f13bc702147cc4fdc09dd6bba81774b1c60a7cbd64c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370324161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d7e48332f115531b67b738e50112a1566f7f29cff6d6b0f0f94199f70bea70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:18:30 GMT
ENV container oci
# Tue, 02 Jun 2026 15:18:31 GMT
COPY dir:a6b2b21a8909319c9461e822bff140e3ef1b61d198a2f277660b14bd1d6a271f in /      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:18:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:cdd42785ebb0fd2c525ecf4a97b6b97bf781caa3b4c77f748f3d95a5a6d4bb88 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:cdd42785ebb0fd2c525ecf4a97b6b97bf781caa3b4c77f748f3d95a5a6d4bb88 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:18:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:18:13Z" "org.opencontainers.image.created"="2026-06-02T15:18:13Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:18:13Z
# Tue, 02 Jun 2026 22:47:03 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:47:03 GMT
ENV NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 02 Jun 2026 22:47:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Tue, 02 Jun 2026 22:47:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 02 Jun 2026 22:47:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 02 Jun 2026 22:47:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:47:08 GMT
WORKDIR /var/lib/neo4j
# Tue, 02 Jun 2026 22:47:08 GMT
VOLUME [/data /logs]
# Tue, 02 Jun 2026 22:47:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 02 Jun 2026 22:47:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:47:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7cd594d4c3afe0f66eb7cfc2a31b3e461f371776f986ab3d5084853335f5d2f7`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 33.0 MB (33037428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d46b44b54b61279b504f6496641d04a0bad3496790f25a862b449187271e19e`  
		Last Modified: Tue, 02 Jun 2026 22:47:32 GMT  
		Size: 99.3 MB (99321488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368d4729af5e85bf3a2888a758a55d16e5f2fe85104c215cc7e00a80b97f4ce`  
		Last Modified: Tue, 02 Jun 2026 22:47:29 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e1de9cdbf42f156f63fcbd503c2102048071e2a5c0789ad64715ae6a62c246`  
		Last Modified: Tue, 02 Jun 2026 22:47:35 GMT  
		Size: 238.0 MB (237955191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:d6ec7718395590e116bb6e61e47933d88600c9c9b07f00c0bbabe94275cae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1755002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d215e44cafd8f169b5d822777c408500666b7e62dfcf5bdf944505a5f9d9a05e`

```dockerfile
```

-	Layers:
	-	`sha256:79cc7bf0f9d16a7fc9c34cbbf3511fa91225ad9ab715e421e0571928127adb93`  
		Last Modified: Tue, 02 Jun 2026 22:47:29 GMT  
		Size: 1.7 MB (1733238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d859df9b43430b08cc5f8214bd9d56fa75b8c860f18efde17b538cc2d7a5ea1c`  
		Last Modified: Tue, 02 Jun 2026 22:47:29 GMT  
		Size: 21.8 KB (21764 bytes)  
		MIME: application/vnd.in-toto+json
