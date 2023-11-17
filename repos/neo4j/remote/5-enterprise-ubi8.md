## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a2a70251e1b3301223a12038044a77cb69d779d26de36636070629817ae14097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:fae3189d39d01bc069a01cfda97c2cd8bfd31e26b7f0ced74a4bd981dde162f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574748162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61bb8b8729a83ea95dd5ed02687e79378aacc1f01ae7ff9b410733f638792d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:58 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:59 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75292d19b6ada0fcf335d32c496f9f7829bfbcd1f356b1bf5bc86ad9a9ac7962`  
		Last Modified: Fri, 17 Nov 2023 04:09:04 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d36c2caa4fefccc3fdce485e834a44f88157e4400a7c95c61a4a2bd5b20351`  
		Last Modified: Fri, 17 Nov 2023 04:09:19 GMT  
		Size: 384.0 MB (383978181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:51a1d4b0c1d0c87f687fb99f20d080e62c900be82e1360482b3c3d7a697d6a8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571856232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa097175b9839a4a175639fdbb1beaeb57c7fce54e3eab45d5d6448d81e9ccf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:25:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:25:00 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:25:01 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:25:01 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:25:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:25:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8afe0f1f1a01988b2e5b24f9e1098e5cd45b2530f7dcf74d2f3d03965cb9470`  
		Last Modified: Fri, 17 Nov 2023 03:26:05 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a154f9e3b2395a9b9803f698016c62421aecbae7a191723ea7bf25cf6c19c794`  
		Last Modified: Fri, 17 Nov 2023 03:26:20 GMT  
		Size: 384.0 MB (383978188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
