## `neo4j:enterprise-ubi10`

```console
$ docker pull neo4j@sha256:36ffbb13eb39891d6f744b6e9265c7c1b1fc911f4e898d7ea41274c46e37d246
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:3d4fb7f0a927b70b309b5353c2b53700a47eab044458c88c636bf1324447ba18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.3 MB (517259974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41acb8491c7ad34cdd8e32cf735a93863bf7323f3aed1eeae6066bb6399c3741`
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
# Mon, 13 Apr 2026 23:59:29 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Mon, 13 Apr 2026 23:59:29 GMT
ENV NEO4J_SHA256=a47e20ec6bd7df9fd11781cba86264d530fd1f605cca817271ff7e5bbc7c3b4a NEO4J_TARBALL=neo4j-enterprise-2026.03.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 13 Apr 2026 23:59:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
# Mon, 13 Apr 2026 23:59:29 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 13 Apr 2026 23:59:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 13 Apr 2026 23:59:48 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Apr 2026 23:59:48 GMT
WORKDIR /var/lib/neo4j
# Mon, 13 Apr 2026 23:59:48 GMT
VOLUME [/data /logs]
# Mon, 13 Apr 2026 23:59:48 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 13 Apr 2026 23:59:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 13 Apr 2026 23:59:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f0c6a9d8564d2a3d188b4b49db41fad56fb7e4756edf376c0ff881d93ab0da5e`  
		Last Modified: Mon, 13 Apr 2026 10:09:42 GMT  
		Size: 34.6 MB (34605867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301491585036579a9311627c5d4dec6a3f163a43a7c760577c05d3494cdd42fa`  
		Last Modified: Tue, 14 Apr 2026 00:00:17 GMT  
		Size: 100.4 MB (100372936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830496c753a228ea41958eb51ffcf7b1ba7ad9aa56389cd5eb5fb8a80066c7df`  
		Last Modified: Tue, 14 Apr 2026 00:00:14 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6699563a8503c20ae5406453282d74274269472ce5162febe3c640bd3e4f01`  
		Last Modified: Tue, 14 Apr 2026 00:00:23 GMT  
		Size: 382.3 MB (382271119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:d7ce952ea99ffe26cb6cf89394af90d98f8f27e7bb70c54ec2ede8cafc95aa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2044063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac7c7ea94eafb79c8b80081d1f8f95812f4b44656967780662e7a0ba45cc98a`

```dockerfile
```

-	Layers:
	-	`sha256:b555b54f0703492e30febd1a430c66abbff14286b6e250c2684423a72cc15b01`  
		Last Modified: Tue, 14 Apr 2026 00:00:14 GMT  
		Size: 2.0 MB (2023660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d308b75a8fdb209c08d9fd73517424e01e885a98ef71b4d325642e8fef4248`  
		Last Modified: Tue, 14 Apr 2026 00:00:14 GMT  
		Size: 20.4 KB (20403 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2e946c41dcc1273aa5dfd103c27bd13e2e120231b729e912adb60148177f7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.0 MB (514013992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a91c59f5f40093195f6a76e524a00aecf5512e52de8858a01ac753bdddfd923`
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
# Tue, 14 Apr 2026 00:01:22 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:01:22 GMT
ENV NEO4J_SHA256=a47e20ec6bd7df9fd11781cba86264d530fd1f605cca817271ff7e5bbc7c3b4a NEO4J_TARBALL=neo4j-enterprise-2026.03.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 14 Apr 2026 00:01:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
# Tue, 14 Apr 2026 00:01:22 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 Apr 2026 00:01:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 14 Apr 2026 00:01:37 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 Apr 2026 00:01:37 GMT
VOLUME [/data /logs]
# Tue, 14 Apr 2026 00:01:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 Apr 2026 00:01:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 00:01:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:412494b6387e552210df602617d718496fdcb1172b467aad0caa041e910fd015`  
		Last Modified: Mon, 13 Apr 2026 11:58:02 GMT  
		Size: 32.7 MB (32680047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c32d12ac24ed1f0f109c4e9428f5dd778af0cbbaaf74a90ad9c48ffd75c7167`  
		Last Modified: Tue, 14 Apr 2026 00:02:09 GMT  
		Size: 99.1 MB (99052746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e60c36398315d017b7e83489d86df1405470e0af581e523653d0a543d249e61`  
		Last Modified: Tue, 14 Apr 2026 00:02:04 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbf1afa2f4b71f1b1cefe5dc52f3b6bc7dd95a9c0dadcd590ef34cdb70fbed3`  
		Last Modified: Tue, 14 Apr 2026 00:02:13 GMT  
		Size: 382.3 MB (382271149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:939ed19b6fb1b5b8b2d78325d5e94b0a4c96ae80e0dc9aa5dda4e687eca7891c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2043427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c9c649ca9429f72f872bf38f5b40a88bdcce33f693536ddeb4be48518f46ec`

```dockerfile
```

-	Layers:
	-	`sha256:e382137595b014cad2176a8e4577f8bb6269d16920927709506a3654d84f6c40`  
		Last Modified: Tue, 14 Apr 2026 00:02:04 GMT  
		Size: 2.0 MB (2022916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d001bcc209d0ada2aa6d9095f8ea9bc7322fa0548ad5cd1a1b19a74f4f4fc1`  
		Last Modified: Tue, 14 Apr 2026 00:02:04 GMT  
		Size: 20.5 KB (20511 bytes)  
		MIME: application/vnd.in-toto+json
