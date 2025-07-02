## `neo4j:2025-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:44c9f43069bc62dc9e07ad995f631ca2d0b37b8757aef5191574a8dd41db99a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:08b63a39fe9cc1e4b570e0828075d0d1c8c3ec396da46ed67e2f28106d621c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.6 MB (508629121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe10393b616c524debc9c1099543570e8fd8e0ff021cb4520e64a6d3689638e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL url="https://www.redhat.com"
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL io.openshift.expose-services=""
# Tue, 24 Jun 2025 16:32:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 24 Jun 2025 16:32:11 GMT
ENV container oci
# Tue, 24 Jun 2025 16:32:12 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Tue, 24 Jun 2025 16:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 24 Jun 2025 16:32:12 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 16:32:13 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 24 Jun 2025 16:32:13 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Tue, 01 Jul 2025 15:46:08 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
ENV NEO4J_SHA256=0dfbe622a001005873bf90fd06b7fedcf4415f6dc9ec31cb35d223304f614f22 NEO4J_TARBALL=neo4j-enterprise-2025.06.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 01 Jul 2025 15:46:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.06.0-unix.tar.gz
# Tue, 01 Jul 2025 15:46:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.06.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 15:46:08 GMT
WORKDIR /var/lib/neo4j
# Tue, 01 Jul 2025 15:46:08 GMT
VOLUME [/data /logs]
# Tue, 01 Jul 2025 15:46:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 01 Jul 2025 15:46:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 01 Jul 2025 15:46:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca15d738476b183e5b14bfa802f5535824a1641fb6ea7ddeaf7752f3b949a69b`  
		Last Modified: Tue, 01 Jul 2025 23:44:35 GMT  
		Size: 136.1 MB (136066556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ca3bd377879148655cb331c8d93ac027653c6c626a1a7647888820ebfc0e66`  
		Last Modified: Tue, 01 Jul 2025 21:40:55 GMT  
		Size: 10.0 KB (9976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df53b0e68a7a81b3a411b5f144983502a0311e4000aaef923e7061a457a25a99`  
		Last Modified: Tue, 01 Jul 2025 23:44:33 GMT  
		Size: 332.9 MB (332901892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7ec7e869897fb7407362096b5ce524a12ea1fd7977477d16721ce4e60feb6529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5941884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3ed46e654d0e18c35d26137ae4f9cce5974f49526b8e84b14902bbdc289b74`

```dockerfile
```

-	Layers:
	-	`sha256:af90020d28d9cb61132557916baee498dc289cfe62d3a4e9f15d379c5193efbd`  
		Last Modified: Tue, 01 Jul 2025 23:43:37 GMT  
		Size: 5.9 MB (5921257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57442f3a26217b5eea9285a70f90ab21b67c37b2d4c56acbac9ff85b9ac9a404`  
		Last Modified: Tue, 01 Jul 2025 23:43:37 GMT  
		Size: 20.6 KB (20627 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7da1ba6b1410fa7672b0558475f083676ed9af8ee228208ddf7a13268e3bd12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.5 MB (501546760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68208cdd4d528d10935bf25e335335db8d9ef54187c86ff808ca0d761767c71e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL url="https://www.redhat.com"
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Jun 2025 13:23:43 GMT
ENV container oci
# Thu, 19 Jun 2025 13:23:43 GMT
COPY dir:837c51d2245269e7540005032254a14f4d0618334b5c45ecacf5b0c7968d0657 in / 
# Thu, 19 Jun 2025 13:23:43 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 19 Jun 2025 13:23:43 GMT
CMD ["/bin/bash"]
# Thu, 19 Jun 2025 13:23:43 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 19 Jun 2025 13:23:43 GMT
LABEL "build-date"="2025-06-24T16:36:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Thu, 19 Jun 2025 13:23:43 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV NEO4J_SHA256=836097f43a9d33f986620f5ff6d7862f83623f6a74d7d828dbe2d694c39f98cd NEO4J_TARBALL=neo4j-enterprise-2025.05.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 19 Jun 2025 13:23:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
# Thu, 19 Jun 2025 13:23:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Jun 2025 13:23:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 19 Jun 2025 13:23:43 GMT
VOLUME [/data /logs]
# Thu, 19 Jun 2025 13:23:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 19 Jun 2025 13:23:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 19 Jun 2025 13:23:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ba92c2079b2b21a2f178ace5ca98b5ef2d5cd02901c30e48729b7afe34ecd27e`  
		Last Modified: Tue, 24 Jun 2025 18:09:22 GMT  
		Size: 37.9 MB (37864307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06470ffc486b55c0f5f01a75d97131f0eb3647b878c412439057c618d37045d5`  
		Last Modified: Thu, 26 Jun 2025 03:02:25 GMT  
		Size: 130.7 MB (130679000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5facace6c31ec368ae3abc5134d19eca32b818c08cff7cdebd7ab8468fb7158`  
		Last Modified: Wed, 25 Jun 2025 23:17:46 GMT  
		Size: 10.0 KB (9979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5faca5c412a77194688af50853472a295d3115a9f48fd1fe012fc43122df85d`  
		Last Modified: Thu, 26 Jun 2025 10:05:51 GMT  
		Size: 333.0 MB (332993442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:07e79b38d266c3200fbaff01550be50f3cc01a854ca1206c7a35ec3d0689ae82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5605129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad484ed1339e5e17acf4be2513aca73d73dfd03db238e07ede2857df6fdf0d0`

```dockerfile
```

-	Layers:
	-	`sha256:4fe7f5e605df1c4e363858981108b8f91551182987003d6636c6cab83df0dd8c`  
		Last Modified: Thu, 26 Jun 2025 02:43:27 GMT  
		Size: 5.6 MB (5584389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db72439a31ec09dde79d77d5705a09aafa5092082c3324f7c7abbf824817bc`  
		Last Modified: Thu, 26 Jun 2025 02:43:28 GMT  
		Size: 20.7 KB (20740 bytes)  
		MIME: application/vnd.in-toto+json
