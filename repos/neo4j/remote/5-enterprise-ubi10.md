## `neo4j:5-enterprise-ubi10`

```console
$ docker pull neo4j@sha256:1f9e0ab26c977c02fc08c56f48de27230063111c911527d251fc518b311ce28d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:4a10a4753503d7ee7c3eda071710db84b6243e4175b357a576ed48cc53226bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616913122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f63f74be0630f980587028a507300fc68f9ff8fd35dfaaf1b0a375b9046eda`
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
# Mon, 11 May 2026 21:56:33 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Mon, 11 May 2026 21:56:34 GMT
ENV NEO4J_SHA256=e417825ffda8b405de7bb7b45788d3810ff270fbe09b7ddc12fb2a6a09de737d NEO4J_TARBALL=neo4j-enterprise-5.26.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 11 May 2026 21:56:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
# Mon, 11 May 2026 21:56:34 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 11 May 2026 21:56:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 11 May 2026 21:56:43 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 21:56:43 GMT
WORKDIR /var/lib/neo4j
# Mon, 11 May 2026 21:56:43 GMT
VOLUME [/data /logs]
# Mon, 11 May 2026 21:56:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 11 May 2026 21:56:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 11 May 2026 21:56:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92d62aafb6a18663d52e4aabc1138a75b2e6994c38e927e9099cb078cc22e6b7`  
		Last Modified: Wed, 06 May 2026 10:14:33 GMT  
		Size: 34.6 MB (34621721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc32fe5f924f3cc83a3bbe840f2839e0fbc6376ffa9791a16c98036a99ab2dab`  
		Last Modified: Mon, 11 May 2026 21:57:13 GMT  
		Size: 86.0 MB (86033384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bccf294e8f486ea040693ffe5008db06dc72c7a15b9f8ce91e2ecc1c78dca6`  
		Last Modified: Mon, 11 May 2026 21:57:09 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436932483ccc822109a1ca6152e717dd6ff11b8b260b2bcff3518a6a34aa798`  
		Last Modified: Mon, 11 May 2026 21:57:21 GMT  
		Size: 496.2 MB (496247922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:2d14ac86bdc5bd85035549d2085e18836e73c13ec0885faae29de429bca653c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1993585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef880538fbf9e0575067275287c9fe9fb0c0d429604177b9a5ea75373010679`

```dockerfile
```

-	Layers:
	-	`sha256:ca08519ea6556ca4e0a12d5a5e10453f3b4b9b2326b6bbff41f065dea8125fe4`  
		Last Modified: Mon, 11 May 2026 21:57:10 GMT  
		Size: 2.0 MB (1973532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3eb9f53972d3371b3a8a7f07918434812f49ac25afab12564aebc6271b3c1f5`  
		Last Modified: Mon, 11 May 2026 21:57:09 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9936974496d533b67e2bdb8765c55a6ce9f2d1de197dd3ea7e699bb035a2b598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.0 MB (613981907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220f090639c92df2eb8b7ac53ad4ece5b678d85742e5f71cd6cdbccc6d5851c1`
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
# Mon, 11 May 2026 21:56:27 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Mon, 11 May 2026 21:56:27 GMT
ENV NEO4J_SHA256=e417825ffda8b405de7bb7b45788d3810ff270fbe09b7ddc12fb2a6a09de737d NEO4J_TARBALL=neo4j-enterprise-5.26.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 11 May 2026 21:56:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
# Mon, 11 May 2026 21:56:27 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 11 May 2026 21:56:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 11 May 2026 21:56:37 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 21:56:37 GMT
WORKDIR /var/lib/neo4j
# Mon, 11 May 2026 21:56:37 GMT
VOLUME [/data /logs]
# Mon, 11 May 2026 21:56:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 11 May 2026 21:56:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 11 May 2026 21:56:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e82aa3f29d1a9f34361831d6ff7b3f84cfd92ed1421ee638f165e55be85bd238`  
		Last Modified: Wed, 06 May 2026 10:17:34 GMT  
		Size: 32.7 MB (32746638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f5863b0fd1d9ba67876b89b9c9fdf86fe1e1dce65ad03fc7ff895444a9dcdd`  
		Last Modified: Mon, 11 May 2026 21:57:10 GMT  
		Size: 85.0 MB (84977258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc825ba5cf2f467f59a2dd01d7c39635ad0842af13f8371d97bd1eef1da3e6e`  
		Last Modified: Mon, 11 May 2026 21:57:06 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4689775792ee9cc63100da12708e5644772796e10b0abecfdd96b20bb92e2df`  
		Last Modified: Mon, 11 May 2026 21:57:20 GMT  
		Size: 496.2 MB (496247918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef414c769bec645993e8d586df2f8db38bff3c514b6ad79334a4d35a4e92b44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1992933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b1bea60e2a5f6937835130506706a723c1abd7d6f3eacd4ed1e186e9961c0f`

```dockerfile
```

-	Layers:
	-	`sha256:9a40f72e1b9715452cbc60beee5f8b381008cba1e0101a0e3caacd0c77c739ba`  
		Last Modified: Mon, 11 May 2026 21:57:06 GMT  
		Size: 2.0 MB (1972779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6f1064c7cd60decb72e4fc4992d4017fadff42e11b74cdc16b03f61ea4fb8a`  
		Last Modified: Mon, 11 May 2026 21:57:06 GMT  
		Size: 20.2 KB (20154 bytes)  
		MIME: application/vnd.in-toto+json
