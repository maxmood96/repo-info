## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json
