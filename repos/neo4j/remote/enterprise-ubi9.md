## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:40d59c97924d201e55d78e02df7de0ffab60fc9ddb9cc67b76f4107347d3785f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c5b96fe713e4b9655e2e87bcb532cf9ed8f2844e205b4f6cf92d39592e2a7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539106492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeea5a2b2292e1680ddf32602c8d092f106211520278f727feea0fc2c00a6fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa282d1d447912112ea82af8315e469d48bf9c8fab8c92078346278d1ca610d`  
		Last Modified: Wed, 29 May 2024 23:01:40 GMT  
		Size: 125.2 MB (125175347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96db6d20d012ffc4596474d7e180f20bbdcc93e5fdcc5ab31e4143fdf4c2be32`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 9.5 KB (9545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f123ac5729d3ca167b4403cc68570dfdf36a4a8999455d488a56276cd726ae`  
		Last Modified: Wed, 29 May 2024 23:01:46 GMT  
		Size: 375.0 MB (375044503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ec9ed2a8fb4cb9a0762655d9b6b1df665b89621055123bb86da65cdf8b9982b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f394fd800b30ae01de41f9c43751677924836e4d53ac8c3803194ada788d34cd`

```dockerfile
```

-	Layers:
	-	`sha256:f7614b5e0f64af0fea72b62fb4ae2444fc559a68d3cc5e570bcd4c892e978db0`  
		Last Modified: Wed, 29 May 2024 23:01:38 GMT  
		Size: 5.2 MB (5220335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d840d67b8fdf084f1e1a970b865a0928e83b9c4d26988598b91f2b3100e195f`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 20.4 KB (20419 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d758b617678b252e51f56d02ea79f0e2d652ecc6599ff561f456cc49a962a7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541859874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930a633e518c25a7e070f6b634a621a22b7c02a63e25abb2476557c0037d6169`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18871374df4282d60741792b044d3274f56b0324c5f3cf1698b2c74d40f70133`  
		Last Modified: Thu, 23 May 2024 20:23:12 GMT  
		Size: 375.0 MB (375044566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7590a61dc4427200797682d8b5ae73e8eededfd36486301a6bd79463d7463549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ed3748b56b01a09823d1f8498f79031bb40c8136d9c08f633164e702dc815`

```dockerfile
```

-	Layers:
	-	`sha256:0fe01a711b7cd3c6ad7a3c46b8afcb7712244791d5ece662bac44e3c570995cb`  
		Last Modified: Thu, 23 May 2024 20:23:03 GMT  
		Size: 5.5 MB (5517615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c35eec85181e213a4cb7c2766b8250d164576294fc367824bd9ec22dbb6d19`  
		Last Modified: Thu, 23 May 2024 20:23:02 GMT  
		Size: 20.4 KB (20429 bytes)  
		MIME: application/vnd.in-toto+json
