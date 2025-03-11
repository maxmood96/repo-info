## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:eb38fdab7556cb652049cb56fd7ae96e5b47bfa0f6e9108613753b46fba93395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:6d77044e47dc02c3891eded284d3837d0ce776ad1b1538bc1d2866c2922237e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333525414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2638da36e8542973a011fbb318b66ee159a8f8d8b66e0e3f672c7e2211e7d6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 24 Feb 2025 12:12:23 GMT
ENV container oci
# Mon, 24 Feb 2025 12:12:23 GMT
COPY dir:a07d6464b408a07384eb87b8e371fb05260f293df1fdae9e20c1a6653e15e37b in / 
# Mon, 24 Feb 2025 12:12:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 24 Feb 2025 12:12:23 GMT
CMD ["/bin/bash"]
# Mon, 24 Feb 2025 12:12:23 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL "build-date"="2025-03-10T09:47:15" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Mon, 24 Feb 2025 12:12:23 GMT
RUN /bin/sh
# Mon, 24 Feb 2025 12:12:23 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
ENV NEO4J_SHA256=1e0b527f0c134869020d3fb1b7af7fa69d93d429117c500f7acce953ee7c7d7f NEO4J_TARBALL=neo4j-community-5.26.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 24 Feb 2025 12:12:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.3-unix.tar.gz
# Mon, 24 Feb 2025 12:12:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Feb 2025 12:12:23 GMT
WORKDIR /var/lib/neo4j
# Mon, 24 Feb 2025 12:12:23 GMT
VOLUME [/data /logs]
# Mon, 24 Feb 2025 12:12:23 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 24 Feb 2025 12:12:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 24 Feb 2025 12:12:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ecb02bde81105b662eaf8da4b200f811c2ac8a0dd37e0c09f19de54603c5c8fb`  
		Last Modified: Mon, 10 Mar 2025 10:32:31 GMT  
		Size: 39.4 MB (39376539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92b0a09d78952dd6b3d60aa8a9f9ef1c8282b59a65bcc5aa506acb82686576`  
		Last Modified: Mon, 10 Mar 2025 10:32:31 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cd9d98bf699e35fe04cbc9d54e006bf0f7f7f994cc1db7bc37821289849167`  
		Last Modified: Mon, 10 Mar 2025 21:08:01 GMT  
		Size: 133.8 MB (133839270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e629747b077a45794762c73f6a5af7d485a710b5b865e3286d924ebf5355846a`  
		Last Modified: Mon, 10 Mar 2025 21:07:57 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb1e7739d209f8026c809acef09728b071b6f0a5eeac37e82cfb6c2b13d28eb`  
		Last Modified: Mon, 10 Mar 2025 21:08:02 GMT  
		Size: 160.3 MB (160299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2349fee281cd52bdff68dee562a5e135c12a4b910a704c01a82ed4db059b7709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6401743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10c88249ca18368b65980ff1f137493e30dd53b658fd26a802b9b12396e3001`

```dockerfile
```

-	Layers:
	-	`sha256:7858325be0275eb506a200cbd14c23704ea8ea98a16389326c41a9c99caa89a1`  
		Last Modified: Mon, 10 Mar 2025 21:07:58 GMT  
		Size: 6.4 MB (6379811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714914c8a128e26664f6e92a375ee19624fb191fc3f75438f9f2dd060d09ca4e`  
		Last Modified: Mon, 10 Mar 2025 21:07:57 GMT  
		Size: 21.9 KB (21932 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:07565681b4e9b66bf6e80a7cb319a4e6e8f752f044b4839df473f20cf7b468e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331744451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b9efce5ec0aeeb7131250cc3911202477d7122b5a669ed907f84c8f8ff242f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 24 Feb 2025 12:12:23 GMT
ENV container oci
# Mon, 24 Feb 2025 12:12:23 GMT
COPY dir:7cf9b7b9f60ce494e82504114b8e4e8497504001337c87ffc50d4a40fe4f9edc in / 
# Mon, 24 Feb 2025 12:12:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 24 Feb 2025 12:12:23 GMT
CMD ["/bin/bash"]
# Mon, 24 Feb 2025 12:12:23 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 24 Feb 2025 12:12:23 GMT
LABEL "build-date"="2025-03-10T09:50:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Mon, 24 Feb 2025 12:12:23 GMT
RUN /bin/sh
# Mon, 24 Feb 2025 12:12:23 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
ENV NEO4J_SHA256=1e0b527f0c134869020d3fb1b7af7fa69d93d429117c500f7acce953ee7c7d7f NEO4J_TARBALL=neo4j-community-5.26.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 24 Feb 2025 12:12:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.3-unix.tar.gz
# Mon, 24 Feb 2025 12:12:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.3-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 24 Feb 2025 12:12:23 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Feb 2025 12:12:23 GMT
WORKDIR /var/lib/neo4j
# Mon, 24 Feb 2025 12:12:23 GMT
VOLUME [/data /logs]
# Mon, 24 Feb 2025 12:12:23 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 24 Feb 2025 12:12:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 24 Feb 2025 12:12:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b8fe7f82e9c2744a37d9d57d915bba00fe3879ae010a254770d6de52407d6b`  
		Last Modified: Mon, 10 Mar 2025 10:36:22 GMT  
		Size: 37.6 MB (37585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b83df990133b9bdb95a233cede88e14a9e9f42d8a90daca3368a0795857bbf6`  
		Last Modified: Mon, 10 Mar 2025 10:36:20 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c90664669f00c2572bddbe2a33a8b55701661ba45b83e86a292c03e93df2ab0`  
		Last Modified: Mon, 10 Mar 2025 22:06:36 GMT  
		Size: 133.8 MB (133849307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dafcc598e7836eadcb1a379f11a30a8ea880e6686f9a1ce4864892b7edfaae`  
		Last Modified: Mon, 10 Mar 2025 22:06:32 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ca1c50b0818bb7685465b7abb15f1eac0a6f970a6192cc1153c639bac0f81`  
		Last Modified: Mon, 10 Mar 2025 22:10:06 GMT  
		Size: 160.3 MB (160299088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7e8de7af5c10ca85ed336cfbcecbd3bf7245c40739f76429488357fbf7b9b155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088f35f94cbba8269787403ea6b5888a73d81f7ad663cf1231df3c6de1f72f7`

```dockerfile
```

-	Layers:
	-	`sha256:d0b248521835037ec8f58b396f324df075f53acc85f085dd747014cbc0d848f1`  
		Last Modified: Mon, 10 Mar 2025 22:10:03 GMT  
		Size: 6.4 MB (6359223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5fdaaad12ebfa9542e15cee280259fc55a1f99dbf039b52cfbbeeb4316a4c1`  
		Last Modified: Mon, 10 Mar 2025 22:10:02 GMT  
		Size: 22.1 KB (22070 bytes)  
		MIME: application/vnd.in-toto+json
