## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:7b46175dfc9855c1d8f462ac381c8fa085319817f6193608c83c86aa1248e047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json
