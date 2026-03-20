## `neo4j:2026-community-ubi10`

```console
$ docker pull neo4j@sha256:ec3e0aa88719a55e6fc3d6873d50ca922b85eb2df7d358192bead7f7ab84a346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-community-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:33f6efb16bb8de26df38bd2217a8881b52a2741df648b8825828ebe015130bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386572074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbf9f6a775b55f5a64cabb3385fede9a0ae2b8ebf5f965cc644f9ec3892437a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:53:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:53:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:53:01 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:53:01 GMT
ENV container oci
# Thu, 19 Mar 2026 04:53:01 GMT
COPY dir:af440ed069b945cf125ef868e769f70d1b1e33071b111d96c1e9a1ffc5f76e4e in /      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:53:01 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:53:01 GMT
COPY file:6585c86973269b2041af40b485e0e6f045b49959f72c04fee4a05795e2e5a97c in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:53:02 GMT
COPY file:6585c86973269b2041af40b485e0e6f045b49959f72c04fee4a05795e2e5a97c in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:53:02 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:52:47Z" "org.opencontainers.image.created"="2026-03-19T04:52:47Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:52:47Z
# Fri, 20 Mar 2026 00:19:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:19:28 GMT
ENV NEO4J_SHA256=4e95626e21348a30109799a44639c2169bc24e27e1a1371972ff2583c3d8493c NEO4J_TARBALL=neo4j-community-2026.02.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 20 Mar 2026 00:19:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
# Fri, 20 Mar 2026 00:19:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 20 Mar 2026 00:19:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 20 Mar 2026 00:19:34 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:19:34 GMT
WORKDIR /var/lib/neo4j
# Fri, 20 Mar 2026 00:19:34 GMT
VOLUME [/data /logs]
# Fri, 20 Mar 2026 00:19:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 20 Mar 2026 00:19:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:19:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f862e22eed3c55bcf45baceaa7dd39dbd424275e0f2d3130583784c94e488dfd`  
		Last Modified: Thu, 19 Mar 2026 06:14:45 GMT  
		Size: 34.6 MB (34610902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fefd7427cd2eb7928a8f4663d07334a35ab3377c62d0ba38c3e9069d2a35a7`  
		Last Modified: Fri, 20 Mar 2026 00:19:59 GMT  
		Size: 100.3 MB (100295210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238620d844cf72e5e0e00b38e91f90e71b199e65a3972a6c536785a2c772098e`  
		Last Modified: Fri, 20 Mar 2026 00:19:55 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c8af7627ac96dccfcc09a90f325dcfe4341f27a416eb7c37884eede129da00`  
		Last Modified: Fri, 20 Mar 2026 00:20:03 GMT  
		Size: 251.7 MB (251655915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e3cea6d4e08f0bab9cce8ee110408005e8321556a653e09e0aa0356d355c97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1769360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af11c7747efaa8f5414fd322d3b0f1a36aff77b0e8edcc3f5e6a2d4ac20441e9`

```dockerfile
```

-	Layers:
	-	`sha256:d885e327f19d863f4d1398588e35db2c80ce5a756c4c286ecfecf6f1bba9c052`  
		Last Modified: Fri, 20 Mar 2026 00:19:55 GMT  
		Size: 1.7 MB (1747754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:871abcf0b8e96c1eb014ca8426791bce2d6be8fdf1a8adec7dcfa01a28396d0e`  
		Last Modified: Fri, 20 Mar 2026 00:19:55 GMT  
		Size: 21.6 KB (21606 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-community-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0f261f8248a3e5967f2b9a559978743b05625bc6f4042234c95714d81b9db5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383322942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17df4dfa83eb48256ae9ead6021df8ed0f799a4936446ef4abeb32034307486`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 04:55:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 04:55:27 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 19 Mar 2026 04:55:27 GMT
ENV container oci
# Thu, 19 Mar 2026 04:55:27 GMT
COPY dir:ddf23ac9073f2f0aebc549dd652158e51758019b3f147b69bcf85b8c51fd9394 in /      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 04:55:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:3038f4da402f5d3deadca7034502c693a744bf96305b10c79908db4a59bf74a2 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:55:28 GMT
COPY file:3038f4da402f5d3deadca7034502c693a744bf96305b10c79908db4a59bf74a2 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 04:55:28 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "org.opencontainers.image.revision"="a7dc8e49f20fc2797d94cac1c236b545b1448291" "build-date"="2026-03-19T04:55:11Z" "org.opencontainers.image.created"="2026-03-19T04:55:11Z" "release"="1773895769"org.opencontainers.image.revision=a7dc8e49f20fc2797d94cac1c236b545b1448291,org.opencontainers.image.created=2026-03-19T04:55:11Z
# Fri, 20 Mar 2026 00:17:30 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:17:30 GMT
ENV NEO4J_SHA256=4e95626e21348a30109799a44639c2169bc24e27e1a1371972ff2583c3d8493c NEO4J_TARBALL=neo4j-community-2026.02.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 20 Mar 2026 00:17:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
# Fri, 20 Mar 2026 00:17:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 20 Mar 2026 00:17:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 20 Mar 2026 00:17:36 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:17:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 20 Mar 2026 00:17:36 GMT
VOLUME [/data /logs]
# Fri, 20 Mar 2026 00:17:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 20 Mar 2026 00:17:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:17:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:32559d11b9ee98b34627afd92e663006f6191d5024358c48c175361f14b3bf84`  
		Last Modified: Thu, 19 Mar 2026 06:26:47 GMT  
		Size: 32.7 MB (32683055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41eddf345f7ffd4e907e4fb0b8a09ddc7182866e7e2e7942e9126eeb4ef88de`  
		Last Modified: Fri, 20 Mar 2026 00:18:01 GMT  
		Size: 99.0 MB (98973924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c338bbdf7aaea8656427af431affb7904c645a864006c95bce9573057050b9`  
		Last Modified: Fri, 20 Mar 2026 00:17:57 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4837ba7b2d133b1d7586567048c70d690f9c4907ab95f24bbb5a1181dd0cc175`  
		Last Modified: Fri, 20 Mar 2026 00:18:06 GMT  
		Size: 251.7 MB (251655911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:29f7de48772ea8bda696643c12586f52d6ffa3a6d81245aa1ee8544970bc4df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757894054918d33490e4fd957288e1dc540a2b2797aa86616703e11d76701324`

```dockerfile
```

-	Layers:
	-	`sha256:2a3634d767c371d5119880c31d21440f9b45832f52a58e8f84594aa53df2dbea`  
		Last Modified: Fri, 20 Mar 2026 00:17:57 GMT  
		Size: 1.7 MB (1747058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709985b598127e2a889fa4ed165ce017a95c4a3d560255cde150f6a0f5be1bb`  
		Last Modified: Fri, 20 Mar 2026 00:17:57 GMT  
		Size: 21.8 KB (21763 bytes)  
		MIME: application/vnd.in-toto+json
