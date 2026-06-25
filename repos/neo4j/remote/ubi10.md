## `neo4j:ubi10`

```console
$ docker pull neo4j@sha256:e47e70d2d06984130503367e0f58896a7813cbffd4c6fa04152c0bf9e754930b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi10` - linux; amd64

```console
$ docker pull neo4j@sha256:59295f2985a94d30f23647a874634314d91def1535d537e85d79b4b9d3611d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.5 MB (373485710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ffdbde61223f7bc4b0c77892c8d741a3cdd026cf95831f10e8acca82129d07`
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
# Wed, 24 Jun 2026 23:06:23 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:06:23 GMT
ENV NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 23:06:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Wed, 24 Jun 2026 23:06:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 23:06:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 24 Jun 2026 23:06:27 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:06:27 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 23:06:27 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 23:06:27 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 23:06:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:06:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d16bd660d5aff2d8cb434aefeedc41e2a96fcbfce0e10b612181d05ae773b985`  
		Last Modified: Wed, 24 Jun 2026 09:11:20 GMT  
		Size: 34.9 MB (34866797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5261137e8eb687a2004de338a4d6dfee7347eb99a34557dc0f73b59ee46ea5`  
		Last Modified: Wed, 24 Jun 2026 23:06:52 GMT  
		Size: 100.7 MB (100653665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906c80639e4b0564c2ab70e41bf0a375d25aa400224a3f6e0addd0c4f1a6e11`  
		Last Modified: Wed, 24 Jun 2026 23:06:48 GMT  
		Size: 10.0 KB (10014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4dc53090057969dbae565c2774bdec32c0891af4447581407597b532a53786`  
		Last Modified: Wed, 24 Jun 2026 23:06:55 GMT  
		Size: 238.0 MB (237955202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:f8ed90c8acbbee0da31cd2948e0e5f8ded8ebbb090a6b11bf109281eb1b10960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1755577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ba046cbdbb01423404a8611875dcd78512dab49ac2b2b15e82df93cf088da0`

```dockerfile
```

-	Layers:
	-	`sha256:c19a562e58c7cc9a26d090a3986051a76c2342bfd93e45822caff01e5627d53e`  
		Last Modified: Wed, 24 Jun 2026 23:06:48 GMT  
		Size: 1.7 MB (1733970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57b773d709dc3d1f281ecdb9d7f62a14f88e1a828bd01bf6fb89047f4f6f516`  
		Last Modified: Wed, 24 Jun 2026 23:06:48 GMT  
		Size: 21.6 KB (21607 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi10` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d290fcf79e893c097d5e354c1816646896209824c5d1bd96458095238363be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.4 MB (370354445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08920ea1be3d6b65fab9780caa0169354db37085e2c2c3ac60bd8297c2b83cf3`
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
# Wed, 24 Jun 2026 23:05:41 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gnupg         gzip         hostname         java-25-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:05:42 GMT
ENV NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 23:05:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Wed, 24 Jun 2026 23:05:42 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 23:05:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi10/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 24 Jun 2026 23:05:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:05:46 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 23:05:46 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 23:05:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 23:05:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:05:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6bcf33c78aa091990500f016c1ed0cb35bc3f67461b918afc9de35f0b601382c`  
		Last Modified: Wed, 24 Jun 2026 09:11:21 GMT  
		Size: 33.0 MB (33046417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef704147fbed920f8afa83d0a741a3dd659a5f8427105eb0780a6518586538`  
		Last Modified: Wed, 24 Jun 2026 23:06:10 GMT  
		Size: 99.3 MB (99342705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85bfaeb628c720802f2180a028f91342549575e8729daaad4bc34717659299`  
		Last Modified: Wed, 24 Jun 2026 23:06:07 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14f4a4d7cf811cb41948d0443768cc96101a80a4471d692d238cd48800fe66e`  
		Last Modified: Wed, 24 Jun 2026 23:06:13 GMT  
		Size: 238.0 MB (237955271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi10` - unknown; unknown

```console
$ docker pull neo4j@sha256:f62b47313cf777aa736ddf7709d88659f5d61cc961e21559e72bb2113a2d55a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1755038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a529ccb336974209d9686b12e0343017e9d371662a6cad47b636459c62d63e`

```dockerfile
```

-	Layers:
	-	`sha256:ba689a5954334bf51e5dba321b40f5ee7994cf5913a7a2586490e822509d0db7`  
		Last Modified: Wed, 24 Jun 2026 23:06:07 GMT  
		Size: 1.7 MB (1733274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cddeddc3c1460fe4e5510fd9b3dc1487e97037d9283bb57ab4c9eb59ac61383`  
		Last Modified: Wed, 24 Jun 2026 23:06:07 GMT  
		Size: 21.8 KB (21764 bytes)  
		MIME: application/vnd.in-toto+json
