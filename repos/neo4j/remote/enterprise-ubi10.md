## `neo4j:enterprise-ubi10`

```console
$ docker pull neo4j@sha256:a01a5118486543502c0f9e47af16f83b5f8402970a6cb2043b3257672c2d03fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:d425a9e2b114287920df4d35764c105f0cc5fda9702288a2f89a2b7430e14a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.6 MB (513640318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d351d143c3531d7b18f69023bb7ad89d45486946d995a7648bf8a3f7baa8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:13:56 GMT
ENV container oci
# Mon, 23 Mar 2026 01:13:56 GMT
COPY dir:e4512bf3738a47eefff7ab81e82e38ca2f5173e43ee99a65e6dd13d89e02bd8f in /      
# Mon, 23 Mar 2026 01:13:56 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:13:57 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:0abc55831e7dab59520989ee7f9e642cfb86d0399f7103e87f7378145dd94508 in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:0abc55831e7dab59520989ee7f9e642cfb86d0399f7103e87f7378145dd94508 in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:13:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:13:42Z" "org.opencontainers.image.created"="2026-03-23T01:13:42Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:13:42Z
# Mon, 23 Mar 2026 18:18:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:18:17 GMT
ENV NEO4J_SHA256=0587f264954dfea33cfec36f442c8aca5156a5db6fbca73d3a3c2523130d2408 NEO4J_TARBALL=neo4j-enterprise-2026.02.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 23 Mar 2026 18:18:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
# Mon, 23 Mar 2026 18:18:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 23 Mar 2026 18:18:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 23 Mar 2026 18:18:27 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:18:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Mar 2026 18:18:27 GMT
VOLUME [/data /logs]
# Mon, 23 Mar 2026 18:18:27 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 23 Mar 2026 18:18:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Mar 2026 18:18:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2979ea27473f21e894361ff5d915252c378d4a8073aca3908465bbbf348780b7`  
		Last Modified: Mon, 23 Mar 2026 03:10:44 GMT  
		Size: 34.6 MB (34630234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d49ce68d00f201b4c0a8bf60d78de7bce1db111aa4caf15b16dfcd10e2cf582`  
		Last Modified: Mon, 23 Mar 2026 18:18:55 GMT  
		Size: 100.3 MB (100307927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e90fa8bab52a390535d3accc3057348b29a651e0307ed5405675c144d5aeb30`  
		Last Modified: Mon, 23 Mar 2026 18:18:51 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5244831d348bcb86405ee77ee2fc3967c12e40fbf15239b29ee2e3f47995d8d`  
		Last Modified: Mon, 23 Mar 2026 18:19:01 GMT  
		Size: 378.7 MB (378692104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:b02f8ff84e827acdc3c9e97636f29dfb3daa39bc3f23ce786ef91908f2e164cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2039403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a3278be661020ee1d8305987dbbaace45180a4f10947e5b63e2bcd6030fea6`

```dockerfile
```

-	Layers:
	-	`sha256:74d447c3f24fe623921a02453a6130ab7318809aca0706b59b531c13658db256`  
		Last Modified: Mon, 23 Mar 2026 18:18:51 GMT  
		Size: 2.0 MB (2019000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4886dc4e2084e00d91573f91939c46055316e89e71c30987f935ddbd1661d43d`  
		Last Modified: Mon, 23 Mar 2026 18:18:51 GMT  
		Size: 20.4 KB (20403 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9233bb94162148434c0496f63f97e3c6d9bcb62b7cc4beddfc0d31624494ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.4 MB (510374994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a1ac6be0383ba66ac78999a7b3d6c1e2bcca5e6c73c9ea0a1aed4f51e1b62e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:17:03 GMT
ENV container oci
# Mon, 23 Mar 2026 01:17:04 GMT
COPY dir:5423a2d232cda7a57202522795efee6ca78fcc0651e41ab821993b780fdf8627 in /      
# Mon, 23 Mar 2026 01:17:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:17:04 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:17:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:c5d7f4f2dd90b98f707a017338d65e0949c625a6c68e260ee9a0d4613ffd89fd in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:c5d7f4f2dd90b98f707a017338d65e0949c625a6c68e260ee9a0d4613ffd89fd in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:17:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:16:47Z" "org.opencontainers.image.created"="2026-03-23T01:16:47Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:16:47Z
# Mon, 23 Mar 2026 18:17:52 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:17:52 GMT
ENV NEO4J_SHA256=0587f264954dfea33cfec36f442c8aca5156a5db6fbca73d3a3c2523130d2408 NEO4J_TARBALL=neo4j-enterprise-2026.02.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 23 Mar 2026 18:17:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
# Mon, 23 Mar 2026 18:17:52 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 23 Mar 2026 18:18:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 23 Mar 2026 18:18:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:18:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Mar 2026 18:18:01 GMT
VOLUME [/data /logs]
# Mon, 23 Mar 2026 18:18:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 23 Mar 2026 18:18:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Mar 2026 18:18:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cbfdca2ca63ac63914141abb4cb933134b748fc3efb6e835daea267d6feb9296`  
		Last Modified: Mon, 23 Mar 2026 03:33:50 GMT  
		Size: 32.7 MB (32686471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce16b1250779f915abefc1fffff5bcb695340bd823e1689ffc543c955fac4086`  
		Last Modified: Mon, 23 Mar 2026 18:18:34 GMT  
		Size: 99.0 MB (98986354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60f367703f85de06c1750c09e4bf5800cf2d4d8fbd5f8350066adb22a8e2d77`  
		Last Modified: Mon, 23 Mar 2026 18:18:26 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d0889f9446c765cc56afef2fb7d2f15317f166f6e0e652430719d3f8ccfb52`  
		Last Modified: Mon, 23 Mar 2026 18:18:34 GMT  
		Size: 378.7 MB (378692121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:6e72143271003cdf9e7166f7d2aabb750adcea0b297b8a3bf43dca02a22ea2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2038768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fd915f0063c2c52297d8756dcd3671e2ce68a64d7ae1c416ed76c82ffda31a`

```dockerfile
```

-	Layers:
	-	`sha256:db91338b5a303c955efc2bb70d44baeba97e46249de86003714e70bab05a4029`  
		Last Modified: Mon, 23 Mar 2026 18:18:26 GMT  
		Size: 2.0 MB (2018256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a125eab564c7e71512a8411f07566e2ca03186010fad4505bb4b5e879029b6`  
		Last Modified: Mon, 23 Mar 2026 18:18:26 GMT  
		Size: 20.5 KB (20512 bytes)  
		MIME: application/vnd.in-toto+json
