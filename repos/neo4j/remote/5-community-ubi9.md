## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:0e057517d3478487e6be0df50c8f15591f5fb962a58c67555cb5a173d73f1f02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:218136af7116ef692a08b749b3e51a784b488492a90ec0d1be6f76885a8b6637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.1 MB (332091876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a352b1628008980bfeea2adf7433ac722d845923149b06828da998b1f570692`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 14 May 2025 10:36:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 14 May 2025 10:36:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:36:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:36:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:36:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:36:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:36:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 14 May 2025 10:36:11 GMT
ENV container oci
# Wed, 14 May 2025 10:36:11 GMT
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Wed, 14 May 2025 10:36:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:36:11 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:36:11 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:36:12 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Tue, 27 May 2025 16:09:55 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV NEO4J_SHA256=0c73f9f06e4720950db49acfb27dc4e7359b8ebd2630810ba3b209e1d269bae2 NEO4J_TARBALL=neo4j-community-5.26.7-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 27 May 2025 16:09:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
# Tue, 27 May 2025 16:09:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 16:09:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 May 2025 16:09:55 GMT
VOLUME [/data /logs]
# Tue, 27 May 2025 16:09:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 27 May 2025 16:09:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 May 2025 16:09:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Wed, 14 May 2025 14:33:02 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b503df9d083dbcfbc91f446d03e7738a0c8a1e7595e2f527e4c1f5ddb47bdfb2`  
		Last Modified: Tue, 27 May 2025 20:45:49 GMT  
		Size: 124.4 MB (124424564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080d522ce43bef2bd6f570cd9997210a0fd6b10b3b6cf94e89148ea7a4e66ff3`  
		Last Modified: Tue, 27 May 2025 20:45:46 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1730f6b85e7cefc0244a2f7af89ca69234cf9d2dc6ab6a9957d9175db39f1`  
		Last Modified: Tue, 27 May 2025 20:45:50 GMT  
		Size: 168.0 MB (168012156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:fddb898086812b3e7ebe9fbb77546d51c3d8f8265d31d28432446bb7e4de53ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d6cc1375042eb4b124d8fee624c6626ce47e6e29c720273ed9e903093632f5`

```dockerfile
```

-	Layers:
	-	`sha256:ffe78a1b7aa37369dba586a567ce28a5f877d64d6a7899940371150321447978`  
		Last Modified: Tue, 27 May 2025 20:45:46 GMT  
		Size: 5.3 MB (5286825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034f4974c3f8ab2c303df1edb58e924e45628cf93bde460443931f364fe51e9b`  
		Last Modified: Tue, 27 May 2025 20:45:46 GMT  
		Size: 21.2 KB (21162 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2421256cf1834447336f3044e97e5436f0d80c5bda421fa0bfed09aaf55519bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330291284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39c1e8bdc7ec65012bd34c7a92cd29db5dbfd299ff8397a54f7acad59ca06bd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 14 May 2025 10:40:48 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 14 May 2025 10:40:48 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:40:48 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:40:48 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:40:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:40:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:40:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 14 May 2025 10:40:48 GMT
ENV container oci
# Wed, 14 May 2025 10:40:49 GMT
COPY dir:3fa6b42aa9cb1575a22397e201df9f16228db85fb99450db2e9f8bef40a52c0f in / 
# Wed, 14 May 2025 10:40:49 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:40:49 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:40:50 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:40:50 GMT
LABEL "build-date"="2025-05-14T10:40:32" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Tue, 27 May 2025 16:09:55 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV NEO4J_SHA256=0c73f9f06e4720950db49acfb27dc4e7359b8ebd2630810ba3b209e1d269bae2 NEO4J_TARBALL=neo4j-community-5.26.7-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 27 May 2025 16:09:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
# Tue, 27 May 2025 16:09:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 16:09:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 May 2025 16:09:55 GMT
VOLUME [/data /logs]
# Tue, 27 May 2025 16:09:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 27 May 2025 16:09:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 May 2025 16:09:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9cf99093c2fb01ee3da769d664a9212c42b7d50516f9e77975132a6540ccdf3b`  
		Last Modified: Wed, 14 May 2025 14:43:12 GMT  
		Size: 37.9 MB (37876105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665d1fd9fc1b5f90e9979d5b2f2c44318b291c5fca5c36b2dc7a2547c6a4ccb3`  
		Last Modified: Tue, 27 May 2025 21:55:28 GMT  
		Size: 124.4 MB (124392983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3277e38f74eb58b28b880db5c1eae942675948cc26eb06ce175cf113e27492`  
		Last Modified: Tue, 27 May 2025 21:55:25 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb79c79968ded64a756b3fb57247ee4519ad771a693bdf3d4ad20fa5dab97d4`  
		Last Modified: Tue, 27 May 2025 21:55:31 GMT  
		Size: 168.0 MB (168012138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:461af8c76659fc9665eeb34dc361ef3b5ac5c1f03b3e04ee848a5d1aaf96f6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887c2a9cc4d4b9cac37a14f53db6a45bd6c805cccdd83999d5f70bfe5e4994f9`

```dockerfile
```

-	Layers:
	-	`sha256:a4447d9c7b30084b23e6e417126113e63c70c219025767aec2542d978980841c`  
		Last Modified: Tue, 27 May 2025 21:55:26 GMT  
		Size: 5.3 MB (5266591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e84f8810153dd91fb361b2c42abb2f454110b6ac736ebd15c743219b4599c559`  
		Last Modified: Tue, 27 May 2025 21:55:25 GMT  
		Size: 21.3 KB (21300 bytes)  
		MIME: application/vnd.in-toto+json
