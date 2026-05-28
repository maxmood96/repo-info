## `neo4j:2026-community-ubi10`

```console
$ docker pull neo4j@sha256:4fb0945a5c33a5ab853835757e171d05b56e1e81630f96c8a92f6d4e67175ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-community-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:bcaea6f4071ba7074bb31b1cfed4080c88a077194ea58af5fa2158294b1bdb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370899664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583b830a7fae476d82a9fdc50b76f027b2eda6526d81f3f010aaa1ce6e3a723e`
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
# Wed, 27 May 2026 22:37:51 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:51 GMT
ENV NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 May 2026 22:37:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Wed, 27 May 2026 22:37:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 May 2026 22:38:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 27 May 2026 22:38:03 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:38:03 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 May 2026 22:38:03 GMT
VOLUME [/data /logs]
# Wed, 27 May 2026 22:38:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 May 2026 22:38:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 May 2026 22:38:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8b457fb1b26320aa35da6d429ea0efa5a81d9f904a24a8d0a4e1a1efcfd0e7b8`  
		Last Modified: Wed, 27 May 2026 07:33:17 GMT  
		Size: 34.9 MB (34902395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d7dbdc731ac3c67d48bb084e9b1a805f6d44b7a67776bb526781b0b4f00865`  
		Last Modified: Wed, 27 May 2026 22:38:27 GMT  
		Size: 100.6 MB (100628042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb884e2fef3cd0492c27fba88cc1b9d6f8e19159ad05ee6c72ef9b59e3b13252`  
		Last Modified: Wed, 27 May 2026 22:38:22 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc644400d078a702fcb48a0c0bd444c795a43f9e497d991c8491192416ee41f`  
		Last Modified: Wed, 27 May 2026 22:38:29 GMT  
		Size: 235.4 MB (235359176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:59f530dabd98780e1c4cd3a83cd40b18dcd4a98d0bccad8a4fd18da01ba7736e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1752841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc52bc8fdc4b6f7f145ac44fa6f450284ca036759869ed89060b6161593b7c2`

```dockerfile
```

-	Layers:
	-	`sha256:e86068a795f5e4c350919539f932441146a0ec6acf866c94ce8ad9bca31f0948`  
		Last Modified: Wed, 27 May 2026 22:38:23 GMT  
		Size: 1.7 MB (1731234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec6ad76827cadd9b0a7b56654c55160c633291a855520367cac76882604f6d25`  
		Last Modified: Wed, 27 May 2026 22:38:22 GMT  
		Size: 21.6 KB (21607 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-community-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1a54814af7832dbb095bf84b78ba8da00db313d2c7dac04c4f52f8bc99a45a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367750664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf72528d4232492b1a163e9c5551a5a3a114655c16aefc0c8aefe902031d698c`
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
# Wed, 27 May 2026 22:38:23 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:38:23 GMT
ENV NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 May 2026 22:38:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Wed, 27 May 2026 22:38:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 May 2026 22:38:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 27 May 2026 22:38:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:38:28 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 May 2026 22:38:28 GMT
VOLUME [/data /logs]
# Wed, 27 May 2026 22:38:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 May 2026 22:38:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 May 2026 22:38:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:94a14999202bc800f78441edfa1b48a3f6b5a799655652a41a4ef92004acb9c3`  
		Last Modified: Wed, 27 May 2026 07:33:15 GMT  
		Size: 33.1 MB (33062079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a81f56f164a4d09e2132869f34f79ba7ce80a00861de9c6ebe177fa62157b`  
		Last Modified: Wed, 27 May 2026 22:38:51 GMT  
		Size: 99.3 MB (99319424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e61a5e790cc00f24369fb7c5808999cf0e298c7fe2ee1fb9ed233f91392516`  
		Last Modified: Wed, 27 May 2026 22:38:48 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9364bac8fd3a59339b04a3c014329c3f5adaee3bbbc2ab23d4802d7d6178de4b`  
		Last Modified: Wed, 27 May 2026 22:38:54 GMT  
		Size: 235.4 MB (235359113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:32bd5ab9a903a54efa5a13dee78f6220a08fa564bc3af58ef187dd5daf513426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1752301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31d05034851bae4973c95c466dece90741edd18238e5371242fde4635ff2b05`

```dockerfile
```

-	Layers:
	-	`sha256:5737f4deb330ec36b20ec68d427c58012a50deec569404ecc3f83aaafbfa93a2`  
		Last Modified: Wed, 27 May 2026 22:38:48 GMT  
		Size: 1.7 MB (1730538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5802e8068d7287a0530fe0196246de4a20eba38c80e9270d25097ece41bef21b`  
		Last Modified: Wed, 27 May 2026 22:38:48 GMT  
		Size: 21.8 KB (21763 bytes)  
		MIME: application/vnd.in-toto+json
