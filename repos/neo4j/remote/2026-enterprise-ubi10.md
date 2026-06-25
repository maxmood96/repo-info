## `neo4j:2026-enterprise-ubi10`

```console
$ docker pull neo4j@sha256:c98603fb8cc095cb19cd7e8844b3b5500595617e9bb983598c26d9ab4be1e763
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:bd7024508125af957802518ed8edf994899a12db5b45120f6e8d72a6a70f24d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.6 MB (519624134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb705e5ed43b3befbaf57bd3250794ba05ff268255f2dbdddc2ecc995f7832c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:40:14 GMT
ENV container oci
# Wed, 24 Jun 2026 06:40:14 GMT
COPY dir:92709e786f8e662d73459e8ec6b629a535dce92ae9fcad21b6d7b00ac6803604 in /      
# Wed, 24 Jun 2026 06:40:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:40:14 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:40:14 GMT
COPY dir:e8e2b7cb869a17d32d7452a63fca2737847da7b62b5d0406fabbac5267964ccc in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:40:15 GMT
COPY dir:e8e2b7cb869a17d32d7452a63fca2737847da7b62b5d0406fabbac5267964ccc in /root/buildinfo/      
# Wed, 24 Jun 2026 06:40:15 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:39:51Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:39:51Z" "architecture"="x86_64" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:39:51Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:06:26 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:06:26 GMT
ENV NEO4J_SHA256=2507ce15c1410931cf81db4435c1e1e437d5a857f59db3f946697988a5263aeb NEO4J_TARBALL=neo4j-enterprise-2026.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 23:06:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
# Wed, 24 Jun 2026 23:06:26 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 23:06:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 24 Jun 2026 23:06:33 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:06:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 23:06:33 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 23:06:33 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 23:06:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:06:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d16bd660d5aff2d8cb434aefeedc41e2a96fcbfce0e10b612181d05ae773b985`  
		Last Modified: Wed, 24 Jun 2026 09:11:20 GMT  
		Size: 34.9 MB (34866797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454e76766a8aee60202f6bd5755f5e589591cbf891bce5b07103f5c1e27b68a`  
		Last Modified: Wed, 24 Jun 2026 23:07:01 GMT  
		Size: 100.7 MB (100653614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4ec419eff72a4eee38594090e8e633c5e90ed4590d1e77fda294a2a07b074`  
		Last Modified: Wed, 24 Jun 2026 23:06:56 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e290d2bdfc6f4d365fe13d0449b3a7090d9c74fff4408064696b203db8991a28`  
		Last Modified: Wed, 24 Jun 2026 23:07:06 GMT  
		Size: 384.1 MB (384093670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:10b09e9b19f1362a96bd14fd97005ced3dba9ce98ad435969a3f48d05fcf4bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc5a2f01f44d47bb228dcd6e81db2722037bcfd82802a4371c59d865ca31169`

```dockerfile
```

-	Layers:
	-	`sha256:7315aa704ccd0e26580c3c5cfbb0499345f88a2f96dc443300c29825ca5b5975`  
		Last Modified: Wed, 24 Jun 2026 23:06:57 GMT  
		Size: 2.0 MB (2034386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892a1052cef6416fa0e6a459117f263ddc697edfebf0ef89bd802af8b932432f`  
		Last Modified: Wed, 24 Jun 2026 23:06:56 GMT  
		Size: 20.4 KB (20403 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:43cb5f1ee999cfa18a8f8b91614452130f9d5a2aca34330707371b7945d5229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516492787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74811695741889321bdcc9865c374c597286fc8495b97a4307f9c5cd5bac278a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:45:18 GMT
ENV container oci
# Wed, 24 Jun 2026 06:45:18 GMT
COPY dir:0b29f9e66bf048f7202a79e2f728b8f136d2a972d39ff75508b0f9653d433ed0 in /      
# Wed, 24 Jun 2026 06:45:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:45:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:45:19 GMT
COPY dir:1852be49c9caac8615951d68388d7f8791140b539cc11bfda91b044119d75a5d in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:45:19 GMT
COPY dir:1852be49c9caac8615951d68388d7f8791140b539cc11bfda91b044119d75a5d in /root/buildinfo/      
# Wed, 24 Jun 2026 06:45:19 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:44:57Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:44:57Z" "architecture"="aarch64" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:44:57Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:05:36 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:05:36 GMT
ENV NEO4J_SHA256=2507ce15c1410931cf81db4435c1e1e437d5a857f59db3f946697988a5263aeb NEO4J_TARBALL=neo4j-enterprise-2026.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 23:05:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
# Wed, 24 Jun 2026 23:05:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 23:05:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 24 Jun 2026 23:05:45 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:05:45 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 23:05:45 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 23:05:45 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 23:05:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:05:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6bcf33c78aa091990500f016c1ed0cb35bc3f67461b918afc9de35f0b601382c`  
		Last Modified: Wed, 24 Jun 2026 09:11:21 GMT  
		Size: 33.0 MB (33046417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7200d182265b6cd0b3b316ee5c637c43a352e5fc69750af2fe99ec65cfa2da`  
		Last Modified: Wed, 24 Jun 2026 23:06:14 GMT  
		Size: 99.3 MB (99342741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7c9922aa31c971fbd2dad6a3996a4f188b1c228fdbf197000b5f29f987c029`  
		Last Modified: Wed, 24 Jun 2026 23:06:11 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea1c3f0b5ac7cec096c25a7d997169750c0562f68f96e7b2b82e0cf5c3b0bf1`  
		Last Modified: Wed, 24 Jun 2026 23:06:19 GMT  
		Size: 384.1 MB (384093578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:dd5ce6d2f4ef2f237779b9914340e337308af2c199ef258df39b4e950b063c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cc5d435d17e8a0926a7b93f7d7cde2aaf5d0174222fb867e92b19a4c925596`

```dockerfile
```

-	Layers:
	-	`sha256:c1dad19982e9304df59a5d61aded39a45813740c8342a3f85508bcc489542efc`  
		Last Modified: Wed, 24 Jun 2026 23:06:11 GMT  
		Size: 2.0 MB (2033642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2426f9c722e06df404d29ba6f26ce58d85209e35dfeb9fc79af7a55bf44e7bc5`  
		Last Modified: Wed, 24 Jun 2026 23:06:10 GMT  
		Size: 20.5 KB (20512 bytes)  
		MIME: application/vnd.in-toto+json
