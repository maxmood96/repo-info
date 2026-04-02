## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:e4c4f731ff7f093bd9cc34ef9a74bda18a4d8fb778b8bb21a24c898045b81619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:54c20b4cbb4b072a2a9c3edbaae54cd0de8b98058ee6ad951ad219465bd119c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.5 MB (374520825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54680d6049b6ed40c2a5c4a190c6588d583171aff97964a7c210e8c3b2c3cf8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Wed, 01 Apr 2026 21:10:10 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 01 Apr 2026 21:10:10 GMT
ENV NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 01 Apr 2026 21:10:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
# Wed, 01 Apr 2026 21:10:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 01 Apr 2026 21:10:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 01 Apr 2026 21:10:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:10:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 01 Apr 2026 21:10:14 GMT
VOLUME [/data /logs]
# Wed, 01 Apr 2026 21:10:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 01 Apr 2026 21:10:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:10:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede7ca16290c1476e747501d61f587cd14804d42ef7097600f77ce8b8a6c08ce`  
		Last Modified: Wed, 01 Apr 2026 21:10:39 GMT  
		Size: 94.3 MB (94263274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb85bf10577f013073a55f53af4646929dff974b0e6edc6b61c93c96e23a876c`  
		Last Modified: Wed, 01 Apr 2026 21:10:35 GMT  
		Size: 10.2 KB (10180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc32c1e3a2be047ef3849b2079fe4a3cc29e03eef882c5090ce3b0ed861f6fa`  
		Last Modified: Wed, 01 Apr 2026 21:10:41 GMT  
		Size: 240.2 MB (240216220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e0553ccd812e49b45e767d07b900f8be23c299a8604036cd870815028f66563b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3934762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb327d6aafdc7a57af80acbffb8f33232f844ac32b3a84a450dd007528493b0a`

```dockerfile
```

-	Layers:
	-	`sha256:d96b42dfbb5e2e88d2629491f43c61c47f540406abee8c5772999ebec8db9b46`  
		Last Modified: Wed, 01 Apr 2026 21:10:35 GMT  
		Size: 3.9 MB (3913231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee99cd3a3e6fefd28b04820b5627802066e9a5d96cd2c91425e813b3ea683f56`  
		Last Modified: Wed, 01 Apr 2026 21:10:35 GMT  
		Size: 21.5 KB (21531 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3e25bbe87f5d8c344c516a102aff4ae5656f2976a616245dcfe8bc96643b7ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371818472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b61d1a9bea38ae098adf1ff84ea5391a46da8925f03cbf70a724017cc5e10a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Wed, 01 Apr 2026 21:10:18 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-x86_64";             suexec_sha="675e7b454ad96e7631029f0b71c9ad5a6c23b553a8952ed528de1e591ca7cef0";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             suexec_url="https://github.com/ncopa/su-exec/releases/download/v0.3/su-exec-static-v0.3-arm64";             suexec_sha="a08773d4af76a30371f8d1c93e86e8ac2b0379c9e75dce9d694c5059b0544909";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gzip         hostname         java-21-openjdk-headless         jq         procps         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     wget -q ${suexec_url} -O /usr/bin/su-exec;     echo "${suexec_sha}" /usr/bin/su-exec | sha256sum -c;     chmod +x /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc;     microdnf clean all # buildkit
# Wed, 01 Apr 2026 21:10:18 GMT
ENV NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 01 Apr 2026 21:10:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
# Wed, 01 Apr 2026 21:10:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 01 Apr 2026 21:10:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 01 Apr 2026 21:10:23 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:10:23 GMT
WORKDIR /var/lib/neo4j
# Wed, 01 Apr 2026 21:10:23 GMT
VOLUME [/data /logs]
# Wed, 01 Apr 2026 21:10:23 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 01 Apr 2026 21:10:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:10:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd8a81bfd23d6178831b1728a01f0886da37901ef197ff2d8c1b4db71304f34`  
		Last Modified: Wed, 01 Apr 2026 21:10:48 GMT  
		Size: 93.4 MB (93387102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e827a08f7d8a35e5d2a41a8697f478e80b872b9b9c2bf32e87efe5debe729141`  
		Last Modified: Wed, 01 Apr 2026 21:10:43 GMT  
		Size: 10.2 KB (10180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631cfd7c2e0d7880cd88ab591c896dd5f7a33f9adb632e6be25f86abdefc901d`  
		Last Modified: Wed, 01 Apr 2026 21:10:52 GMT  
		Size: 240.2 MB (240216256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:536d5a19369011ac8011a0fd10fe51cefcd00ee1f7890c10e8be8cb3da0d8d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdaca08a5de337e627cf63eac7908be2b2d334f4ffaf28f982dc6d91832fe82`

```dockerfile
```

-	Layers:
	-	`sha256:e6739ccd65e91b0c12f8279186e581077a3b5ba407768a5409a18d602cd9dc5d`  
		Last Modified: Wed, 01 Apr 2026 21:10:44 GMT  
		Size: 3.9 MB (3911277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736e70f7ed19346b5968c19f19c58ef6e9c50c202a04e33874bce61aa36957f1`  
		Last Modified: Wed, 01 Apr 2026 21:10:43 GMT  
		Size: 21.7 KB (21692 bytes)  
		MIME: application/vnd.in-toto+json
