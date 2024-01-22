## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:208c3ed5da6cbf2edbe40b2862b7d29eddbd0302342344972c8a33584dd96dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:59fded3746220789b2fdadd2631843ed20b9bc8484612c828c895de0ead03c05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560021769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1820a8a7e17954c9b2c658e3895657e19ff1247c60ac734cd89d36afca69c6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:04 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:16 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:16 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5435e73e2a0cd9b7940e79edf658fb2d75ebffa747232a4fe91a0d125820ab`  
		Last Modified: Mon, 22 Jan 2024 19:51:31 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c39c2b4ae5ca8cf86a701272004e04d8f68fa55585be237152b2b6b02ef20`  
		Last Modified: Mon, 22 Jan 2024 19:51:46 GMT  
		Size: 368.5 MB (368496491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e5c0b51f3107a46c11c7b6685bc64ccc9e2c350bd74257e316716966c959c155
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556896197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c1d23e0e8fc1d167d73d42f33484d49d4f8304c68612f89efbe6485bc4dde2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:50:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:50:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:50:02 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:50:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:50:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:50:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:50:14 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:50:14 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d832087479e0dd60463c20faa5ab722705448985bac6c6ec1b5b6530a64b8e`  
		Last Modified: Mon, 22 Jan 2024 19:52:20 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf706e61d45631559eb7da7b20786928036d40388cf8f7d05b9e0dd9bcbc74`  
		Last Modified: Mon, 22 Jan 2024 19:52:32 GMT  
		Size: 368.5 MB (368496571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
