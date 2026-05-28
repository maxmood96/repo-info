## `neo4j:5-community-ubi10`

```console
$ docker pull neo4j@sha256:332f4ec006a32d776ebcea848ebb82eb2827a8b8b0d45f04657f864f6544762a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:679b439c9019f7174f216dbdb4dd56b00f3fbc40627e543c7b8bcdb1dfbaebd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272818847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ccc1c672c156601761cc3c5307e5b934a2dd7233b537d3e1503678832ddc2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 May 2026 06:12:12 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:12:12 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:12:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:12:12 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:12:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:12:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:12:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:12:12 GMT
ENV container oci
# Wed, 27 May 2026 06:12:12 GMT
COPY dir:8cc023cf96d9d3899063545e0c3b25ee410727bc8ef5903cc1b3e3e22d98dc1f in /      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:12:13 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:12:13 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:919ce0635818e127299907aac3d5ec8b04328702d69e0d804c99d87a631c2e20 in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:919ce0635818e127299907aac3d5ec8b04328702d69e0d804c99d87a631c2e20 in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:12:13 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:11:58Z" "org.opencontainers.image.created"="2026-05-27T06:11:58Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:11:58Z
# Wed, 27 May 2026 22:37:57 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:57 GMT
ENV NEO4J_SHA256=dfc04996dbdab58a9b8a7d7dc2c6bbcad61c55d58a0c296197206135cd888c90 NEO4J_TARBALL=neo4j-community-5.26.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 May 2026 22:37:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.26-unix.tar.gz
# Wed, 27 May 2026 22:37:57 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 May 2026 22:38:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.26-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 27 May 2026 22:38:00 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:38:00 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 May 2026 22:38:00 GMT
VOLUME [/data /logs]
# Wed, 27 May 2026 22:38:00 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 May 2026 22:38:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 May 2026 22:38:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8b457fb1b26320aa35da6d429ea0efa5a81d9f904a24a8d0a4e1a1efcfd0e7b8`  
		Last Modified: Wed, 27 May 2026 07:33:17 GMT  
		Size: 34.9 MB (34902395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2acb7c4a6d234c8921aea6345905188a5c8b81becc63662ff430125a8e8f11`  
		Last Modified: Wed, 27 May 2026 22:38:19 GMT  
		Size: 86.2 MB (86203170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5f6efe7d0fc49adb1196a8d89846ad95feef0cda7dfaa367f8c9e967af2b38`  
		Last Modified: Wed, 27 May 2026 22:38:16 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc13e8f88d51cafbb74afb2d8762dce5744d3c57417f9976de6cf33115b0c2`  
		Last Modified: Wed, 27 May 2026 22:38:20 GMT  
		Size: 151.7 MB (151703187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:9ec0001665b566559667e2b1add8478e2204fe8afbb595514d13b5e8268bf5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1635037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccd367175fa69188c589c83d1ddfd223cb50d4674068e6987f9c650d77624d0`

```dockerfile
```

-	Layers:
	-	`sha256:065acedb6724f4f47f5560fef17c06aa5f340e8404f8ece3eb8be40ecda63c1a`  
		Last Modified: Wed, 27 May 2026 22:38:16 GMT  
		Size: 1.6 MB (1614089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a2c3e14e6afa7a27e42ca9014718e6dcf073acec50419b6ae8d67e53e9d407`  
		Last Modified: Wed, 27 May 2026 22:38:17 GMT  
		Size: 20.9 KB (20948 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d36bf9f7fb073a945da5de0aa0bab0c5c5c15791a51650173ff93c9ec09d5ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269918461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c4adee1c5cc71db33bc9ecb9f83d3dba7fc5afa259c5b83d296ec9cb524163`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 May 2026 06:14:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:14:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:14:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:14:32 GMT
ENV container oci
# Wed, 27 May 2026 06:14:33 GMT
COPY dir:144798cc4c14efe6d25c10c7a6f149af1045784afd86a94e99d04f534f9bbb05 in /      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:14:33 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:14:17Z" "org.opencontainers.image.created"="2026-05-27T06:14:17Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:14:17Z
# Wed, 27 May 2026 22:38:24 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:38:24 GMT
ENV NEO4J_SHA256=dfc04996dbdab58a9b8a7d7dc2c6bbcad61c55d58a0c296197206135cd888c90 NEO4J_TARBALL=neo4j-community-5.26.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 May 2026 22:38:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.26-unix.tar.gz
# Wed, 27 May 2026 22:38:24 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 May 2026 22:38:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.26-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 27 May 2026 22:38:27 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:38:27 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 May 2026 22:38:27 GMT
VOLUME [/data /logs]
# Wed, 27 May 2026 22:38:27 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 May 2026 22:38:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 May 2026 22:38:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:94a14999202bc800f78441edfa1b48a3f6b5a799655652a41a4ef92004acb9c3`  
		Last Modified: Wed, 27 May 2026 07:33:15 GMT  
		Size: 33.1 MB (33062079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09ea0fb79e37cedbb2298d820d780d8f0382deb0bace1421bc58dc9c22fbb7c`  
		Last Modified: Wed, 27 May 2026 22:38:46 GMT  
		Size: 85.1 MB (85143149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572debe9bcbe4233c657a0710b4b22a846da436ece8b2fe6e81569fe6ef7bacb`  
		Last Modified: Wed, 27 May 2026 22:38:43 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccb85627f0ae7a6f9f5e54bcfa626a6dd83e180525a9c29c85f8b031bb99b7b`  
		Last Modified: Wed, 27 May 2026 22:38:48 GMT  
		Size: 151.7 MB (151703139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:e46eabaeb8692f1f31bb4f3260209f19292fc97be3f871ae07d60c3ce6bed888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 MB (1634458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe7ee74e734d057ebd45fc4132777cc24bad2254f2e39cb2332a761ae58b171`

```dockerfile
```

-	Layers:
	-	`sha256:7bccef90866b517a2c316f2aff9f5e979b850680bbb7aa0aca6cb78e8c758da6`  
		Last Modified: Wed, 27 May 2026 22:38:43 GMT  
		Size: 1.6 MB (1613372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9abce90edaba01a2ed662d3d3f497b85e3a4d693c93ea5605beb53d9b5a0c7f`  
		Last Modified: Wed, 27 May 2026 22:38:43 GMT  
		Size: 21.1 KB (21086 bytes)  
		MIME: application/vnd.in-toto+json
