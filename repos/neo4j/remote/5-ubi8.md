## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:5e6ab1589401a8e7de61b454d0b74cf1480af1532f4f2a38b5f141d0de8eefd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7382de285822cea48af9c2b3f3a28189217322bd01638d1a3ac2197c20b94df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330342960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969d1153f15363e78bb0de242e7f3dc3fff961ad33865029edee274e011234d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:06 GMT
ADD file:1e33171104997f0a23d074b9a14db4a4771951c35437300603bf95dc6e59cb86 in / 
# Tue, 14 May 2024 18:16:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:08 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:08 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:08 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:08 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:08 GMT
ENV container oci
# Tue, 14 May 2024 18:16:08 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:08 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:09 GMT
ADD file:a9412abf195f6cf63b75397952b33f829a9372edd9dd4effce36817f4f80f248 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:09 GMT
ADD file:3b0ec9f0d37da7a6f59430134740c3967cbd97a86ad4dcfb8850cecebafe2129 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:09 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:11 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:9d49001ad6c59e36fff8fa74763be0954414b6ad5333f7855bb70fa0d6e86cb6`  
		Last Modified: Wed, 22 May 2024 13:49:28 GMT  
		Size: 39.4 MB (39378105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5268453fc4b751e3223c640622290cfaf5b5b8f07d48acf81abc48aa03bbcdf3`  
		Last Modified: Thu, 23 May 2024 19:53:40 GMT  
		Size: 164.5 MB (164517414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a00b593d87f91b2d62de7cf750304f9a6c0788608b5be1a5ade7120423d90c`  
		Last Modified: Thu, 23 May 2024 19:53:38 GMT  
		Size: 9.7 KB (9719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655046e678bbbad46e550146df1679ed6db51007a10de417e0b29ce19f5753d6`  
		Last Modified: Thu, 23 May 2024 19:53:40 GMT  
		Size: 126.4 MB (126437690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:e477f7155be19e7268fe06976856bfbed348872ccb253449c5afe919b6021df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10860116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd90732b0f8bdd7318a65c7918008fe11eea2d929c07d63a39bf4037107a3ed`

```dockerfile
```

-	Layers:
	-	`sha256:0714f28ec037c2f7f8bee6720a416cda22674b145d80f680aa13eb9c2105e39e`  
		Last Modified: Thu, 23 May 2024 19:53:38 GMT  
		Size: 10.8 MB (10838476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b9d709d6df62a14e73878d990cff106e4feb136666c83363f0ede5ae2ccc04`  
		Last Modified: Thu, 23 May 2024 19:53:38 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json
