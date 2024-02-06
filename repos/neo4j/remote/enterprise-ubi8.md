## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:171f178499473dd06a8dab34504647e5dad9dae101218d14bf91220dedd9eea8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:76eba00f670055a7031e311b9857a123f839851b74b0c424379ef0684e1dec00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.4 MB (560399945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f6ae362f22081125e3d8fcc2324e34114ac5e54388abe0d2f67d97143abe1f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9fc614aeee553d48c4ba1d6fbee0091ec5ff22e9e019e529cab743b3ebae0539 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:a79c0caed99c0b965df6d403d66a01ffc482f1f7855153a88e66f16dd95158e0 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:66b2f11499ec394f464b835b91ff23905b0f8a2606d73f48ac2a8dbd5a7c1480 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706691034.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:7d456cd2c5e8a0a52bd82a0176576d9cfb0e92e69694169d89d1b77b66ccedbb in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706691034 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706691034" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-31T08:51:16" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706691034"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2724420-616b2.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8d18f2ad8b6ae23ad8d28b46586fd090c191afca2585b229687ab8240d089013`  
		Last Modified: Thu, 01 Feb 2024 07:58:07 GMT  
		Size: 39.3 MB (39296077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c79bb6193edb89e44040274c315ad7d043a460681dfef0624b51d63e1a9b2ed`  
		Last Modified: Thu, 01 Feb 2024 20:57:34 GMT  
		Size: 152.6 MB (152598049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d32ac0e5ef304cca899600ae6f64cf103622dc45b9d0abfe7f38df0ad8804f`  
		Last Modified: Thu, 01 Feb 2024 20:57:31 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4923dc420eaf729ca5b2ecd8ee76525335e030edc359a60110a5a42b704ffb`  
		Last Modified: Thu, 01 Feb 2024 20:57:38 GMT  
		Size: 368.5 MB (368496335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:cbd1bc55a9e904f3596c431d952664f88f0041c8d8002c9cf6cf94a9374aac3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9025043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0320e407b4dc046fde064733ac9fec63713fe31ed3d5f18d295ba38b5dd382`

```dockerfile
```

-	Layers:
	-	`sha256:702b4e1f20be9121e9e7db1cf1da6326b74bbad6c0f7d45beb27b7a3f64a55fc`  
		Last Modified: Thu, 01 Feb 2024 20:57:31 GMT  
		Size: 9.0 MB (9004806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:385504e45399f4e14d7fdd15ba0ef6cdf3afc04b6c4560f617be6e9ec9511295`  
		Last Modified: Thu, 01 Feb 2024 20:57:31 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json
