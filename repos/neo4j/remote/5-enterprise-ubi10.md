## `neo4j:5-enterprise-ubi10`

```console
$ docker pull neo4j@sha256:de2d2663e069e56ac63632679dd2079823c6cea47d5d6da403c6d1e4d77de10d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:2366a322a90be348b42f124396bf0591baaba1cfd601bc47d679d443eacee8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.6 MB (632588742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b3dec82c760b9fd20b72dcd33fac7b892f5885754e725e98d2b3438e63e679`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:14:03 GMT
ENV container oci
# Mon, 13 Apr 2026 09:14:04 GMT
COPY dir:76b09a495622d7b6331e3b1ce0727af742be820fe3eaf865e896be5c160bcdbe in /      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:14:04 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:95047be8e40b1e3c668ac62dda8bcb33d863723da6a80c1b3ce4f34f04292a93 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:95047be8e40b1e3c668ac62dda8bcb33d863723da6a80c1b3ce4f34f04292a93 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:14:05 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:13:50Z" "org.opencontainers.image.created"="2026-04-13T09:13:50Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:13:50Z
# Tue, 14 Apr 2026 00:00:34 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:00:34 GMT
ENV NEO4J_SHA256=0c97832ac9dd7172c2315c58b957c343644d4f50a863951976bb1b25ba291f5a NEO4J_TARBALL=neo4j-enterprise-5.26.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 14 Apr 2026 00:00:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
# Tue, 14 Apr 2026 00:00:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 Apr 2026 00:00:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 14 Apr 2026 00:00:45 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:00:45 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 Apr 2026 00:00:45 GMT
VOLUME [/data /logs]
# Tue, 14 Apr 2026 00:00:45 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 Apr 2026 00:00:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 00:00:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f0c6a9d8564d2a3d188b4b49db41fad56fb7e4756edf376c0ff881d93ab0da5e`  
		Last Modified: Mon, 13 Apr 2026 10:09:42 GMT  
		Size: 34.6 MB (34605867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053ca66b59906286e38c280bcd24dff9c44c80f6660767cd3f4e4ada3353d915`  
		Last Modified: Tue, 14 Apr 2026 00:01:16 GMT  
		Size: 85.9 MB (85871779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28985a9960981daab9d4dbe2be3496f91b903d0d3676a1516ff3e990ec4ce7c5`  
		Last Modified: Tue, 14 Apr 2026 00:01:13 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b701b69311d11be3f74197ef059e52493b8cabb1c911cb2f496bdebce70463b7`  
		Last Modified: Tue, 14 Apr 2026 00:01:25 GMT  
		Size: 512.1 MB (512101002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ecb81d038ba3b523cbb25509602edf132b0862a579af1467dfe8860a3081311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b731cda3aaa980feec4ddaa34e0a852af80a05e067cd9bae45c32089229a1e`

```dockerfile
```

-	Layers:
	-	`sha256:5b66be159a472200805cbedd39a6837ef9a2130bfa980e16833808952bbd3b6d`  
		Last Modified: Tue, 14 Apr 2026 00:01:13 GMT  
		Size: 2.0 MB (1981869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a524bb7a4b46e5bcc7d913f68c146e402b8df52b26466076a706d5793198153`  
		Last Modified: Tue, 14 Apr 2026 00:01:13 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:486b4f1ca3055a734cd0312e6a7daffc68461d2c3ffdd5854ec59da3c4884ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.6 MB (629596187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4a9816e774c229551e70e7b90558bcf8b20ce4957edd17c79979347e93f3e4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:16:58 GMT
ENV container oci
# Mon, 13 Apr 2026 09:16:58 GMT
COPY dir:e4f84a8805207b4cd31715d3ea15f1b5641e6568c620ec6afade1b03163f2ec3 in /      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:16:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:d8a3d61eb5d229916123ad1cb0753c18ec7103c4e50b2eea20333708695dac3e in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:d8a3d61eb5d229916123ad1cb0753c18ec7103c4e50b2eea20333708695dac3e in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:16:59 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:16:42Z" "org.opencontainers.image.created"="2026-04-13T09:16:42Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:16:42Z
# Tue, 14 Apr 2026 00:01:26 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:01:26 GMT
ENV NEO4J_SHA256=0c97832ac9dd7172c2315c58b957c343644d4f50a863951976bb1b25ba291f5a NEO4J_TARBALL=neo4j-enterprise-5.26.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 14 Apr 2026 00:01:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
# Tue, 14 Apr 2026 00:01:26 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 Apr 2026 00:01:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 14 Apr 2026 00:01:36 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:36 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 Apr 2026 00:01:36 GMT
VOLUME [/data /logs]
# Tue, 14 Apr 2026 00:01:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 Apr 2026 00:01:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 00:01:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:412494b6387e552210df602617d718496fdcb1172b467aad0caa041e910fd015`  
		Last Modified: Mon, 13 Apr 2026 11:58:02 GMT  
		Size: 32.7 MB (32680047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90e3bd34981272ccab1a932f37e88eed09f4ce690cd37e9db8f8da63b0260a`  
		Last Modified: Tue, 14 Apr 2026 00:02:08 GMT  
		Size: 84.8 MB (84804936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4198beba0470812d9360ba6792ec147a5313ea8a0cf7fefc3b103c7254f0e2ed`  
		Last Modified: Tue, 14 Apr 2026 00:02:05 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f175771453560528c513b35386db6467717138fab9de594b81cfad09a968847`  
		Last Modified: Tue, 14 Apr 2026 00:02:17 GMT  
		Size: 512.1 MB (512101110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:d4d06c4b0f447400d2930412a86a977938bd9dcddbbe75fc734007da244000c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb4ac596c0d418a8090cdafe9c857eee08220e1fc839d1504d42d15fca946b6`

```dockerfile
```

-	Layers:
	-	`sha256:3d4b8bccc428d86fbc01bf437aca05915d21576169f9de1e56c3a7008c184faa`  
		Last Modified: Tue, 14 Apr 2026 00:02:05 GMT  
		Size: 2.0 MB (1981116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b07172554aec1f9f099bbe14c3b86183f9281e6bb2e1e7e4d42a929e1c069b7`  
		Last Modified: Tue, 14 Apr 2026 00:02:05 GMT  
		Size: 20.2 KB (20154 bytes)  
		MIME: application/vnd.in-toto+json
