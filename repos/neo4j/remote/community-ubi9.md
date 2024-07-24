## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:6f0f7a2dca3519f5f5aa45d237d1abddc50ede17058336cbec63e4208342251a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:1248d568f58717dddfe0c7bffcb3c031b24973491b851be6d77fe200af41d8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288594359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674043d262da20d0ae62d10433379740d132cbb0eaec94a985f43411658ee830`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Jul 2024 13:55:16 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV NEO4J_SHA256=80ae623641a3b353e3b2bca5e49cb6f0dbb79d89d512850c751c356a1378c444 NEO4J_TARBALL=neo4j-community-5.22.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 23 Jul 2024 13:55:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
# Tue, 23 Jul 2024 13:55:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 13:55:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 Jul 2024 13:55:16 GMT
VOLUME [/data /logs]
# Tue, 23 Jul 2024 13:55:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 23 Jul 2024 13:55:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f19613916a5b7fb7b5abf48bc9fd27064b445cb40d8566117515f912eef1aab`  
		Last Modified: Tue, 23 Jul 2024 18:13:58 GMT  
		Size: 125.1 MB (125062305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6f95265b268f3d27c09c6ef3adfb273dda22a42e11a91dadf607011887177f`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddd991afd74c16b387aabdfaa63755d8c815f18e6fef30ad7644fb2dc3c1daa`  
		Last Modified: Tue, 23 Jul 2024 18:13:58 GMT  
		Size: 124.7 MB (124670078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:61b2c025621b6376406e0270e7fa29b846f7383a1af5bda9ac483a94427a2916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e0a5a77cd7d16ec0aaf18a3ca587d26fc72925e11aac166006920a2fad5b12`

```dockerfile
```

-	Layers:
	-	`sha256:0673eff10b4e4228c3ad5e55725c78104ca740f3dd7ce3be5ec9deff9a7c7f06`  
		Last Modified: Tue, 23 Jul 2024 18:13:56 GMT  
		Size: 5.1 MB (5122025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824ac31fcf96215ec9476ffd0480b9976daf49ead4661966c8cff959d2ad207d`  
		Last Modified: Tue, 23 Jul 2024 18:13:55 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9ac6891753d0855f00b36c77587162bdfb0e2afe71ed6cd98714fbc01ed560e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282413561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fa13e4ff4ad23e16884c80bf84fbc77085e4ffa5b6db37c06b39c3e092832`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Jul 2024 13:55:16 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV NEO4J_SHA256=80ae623641a3b353e3b2bca5e49cb6f0dbb79d89d512850c751c356a1378c444 NEO4J_TARBALL=neo4j-community-5.22.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 23 Jul 2024 13:55:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
# Tue, 23 Jul 2024 13:55:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 13:55:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 Jul 2024 13:55:16 GMT
VOLUME [/data /logs]
# Tue, 23 Jul 2024 13:55:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 23 Jul 2024 13:55:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec263feba0bc6a13be2e9fd0f8999a0050e950cfaddfa6d15b85fbeafcaf258e`  
		Last Modified: Wed, 24 Jul 2024 12:53:06 GMT  
		Size: 120.6 MB (120618826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5bc09a603cf2ef3e7edb735ba77fc6295a76adbd10cfa5198bd373e92f86fb`  
		Last Modified: Wed, 24 Jul 2024 12:53:03 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc42b477e89d31daf2b91414789281802e539131e21f81c4d82e3505798b4d`  
		Last Modified: Wed, 24 Jul 2024 12:53:06 GMT  
		Size: 124.7 MB (124666684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3facabc1c540032756c2c7ce2345dc3abacb13539f038df29ca94a63fe7da73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ebed3c9b768a35ac9a41823760795aec7b5edcfcb393f75b7fd767c835d553`

```dockerfile
```

-	Layers:
	-	`sha256:6722908dafa2520e183b9c0a7e48bcc0443ad36a8e168185710cb02df7bd99e5`  
		Last Modified: Wed, 24 Jul 2024 12:53:04 GMT  
		Size: 4.9 MB (4865578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825666684ef7e18e0b2166ec68937ddf81c12b27b1514439e1eaa56f3877c002`  
		Last Modified: Wed, 24 Jul 2024 12:53:03 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json
