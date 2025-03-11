## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:eb61841ca9c3132a408e817911c0d32a9dcc2939ac965fc3b58390ab3344a564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:66b75c3a573526327d120498ec978f2298140450f12493aab4352a80355980f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.0 MB (614025913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48743ff8941ecc483a6319335abae7b659f3d155c4b43fd264dfd7470c09ca2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL url="https://www.redhat.com"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.openshift.expose-services=""
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 27 Feb 2025 14:20:06 GMT
ENV container oci
# Thu, 27 Feb 2025 14:20:06 GMT
COPY dir:a07d6464b408a07384eb87b8e371fb05260f293df1fdae9e20c1a6653e15e37b in / 
# Thu, 27 Feb 2025 14:20:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 14:20:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL "build-date"="2025-03-10T09:47:15" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 27 Feb 2025 14:20:06 GMT
RUN /bin/sh
# Thu, 27 Feb 2025 14:20:06 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV NEO4J_SHA256=d4323822935d7677ae5a12dd5638a1ed7012c190b6dd93913640ac2fda30501f NEO4J_TARBALL=neo4j-enterprise-2025.02.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Feb 2025 14:20:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
# Thu, 27 Feb 2025 14:20:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 14:20:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Feb 2025 14:20:06 GMT
VOLUME [/data /logs]
# Thu, 27 Feb 2025 14:20:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Feb 2025 14:20:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 14:20:06 GMT
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
	-	`sha256:578243ff0bd1eff697f4be34a6f033e7d55ca4fdae4972446f544893289a3525`  
		Last Modified: Mon, 10 Mar 2025 21:06:59 GMT  
		Size: 140.5 MB (140484754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44137a6e4b19fad7a8a4743c4bae1b09c59b6fbad66e3369137796b6666755c4`  
		Last Modified: Mon, 10 Mar 2025 21:06:55 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d888df1c67480f223789333de407daf1a09e9d58759b991fafd8c8341476302e`  
		Last Modified: Mon, 10 Mar 2025 21:07:04 GMT  
		Size: 434.2 MB (434154095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f74434448946176f2f315f9f6a4e988b8fe62a00e6538c8372ad1a671aaa9e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6696022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672fc88f44c34c4a89c1d59b90aa817868861db3188c5f34af69796e3f3f84f2`

```dockerfile
```

-	Layers:
	-	`sha256:5523678f2088b06e2ff873c6cf25f790039826cf61d3761cdfad0ae105ecb82e`  
		Last Modified: Mon, 10 Mar 2025 21:06:55 GMT  
		Size: 6.7 MB (6674622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebda7a0995aed9e33dbd6ff4f80138e7ceba7fd1279ed61c9ac7520eb84c9bd`  
		Last Modified: Mon, 10 Mar 2025 21:06:55 GMT  
		Size: 21.4 KB (21400 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6518ee7c6a9658fdd78e30932a9ad8b6820e3be34d0ed7e4694d17dcd84c7789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611917260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abce772f0dda65123e019a68c39cf3370c79f3400d3c4510ae8d91c0e44ab1bd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL url="https://www.redhat.com"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.openshift.expose-services=""
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 27 Feb 2025 14:20:06 GMT
ENV container oci
# Thu, 27 Feb 2025 14:20:06 GMT
COPY dir:7cf9b7b9f60ce494e82504114b8e4e8497504001337c87ffc50d4a40fe4f9edc in / 
# Thu, 27 Feb 2025 14:20:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["/bin/bash"]
# Thu, 27 Feb 2025 14:20:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 27 Feb 2025 14:20:06 GMT
LABEL "build-date"="2025-03-10T09:50:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 27 Feb 2025 14:20:06 GMT
RUN /bin/sh
# Thu, 27 Feb 2025 14:20:06 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-21-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV NEO4J_SHA256=d4323822935d7677ae5a12dd5638a1ed7012c190b6dd93913640ac2fda30501f NEO4J_TARBALL=neo4j-enterprise-2025.02.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Feb 2025 14:20:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
# Thu, 27 Feb 2025 14:20:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 14:20:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Feb 2025 14:20:06 GMT
VOLUME [/data /logs]
# Thu, 27 Feb 2025 14:20:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Feb 2025 14:20:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 14:20:06 GMT
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
	-	`sha256:c4dbebeb21085e99af88ee26740a74005fc4ab3dd5513c249270a4e7532651a3`  
		Last Modified: Mon, 10 Mar 2025 22:09:04 GMT  
		Size: 140.2 MB (140167083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba63e1fb743108aee7860238972cc7da238a4de6c080b011ed653cda5731a96`  
		Last Modified: Mon, 10 Mar 2025 22:08:58 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc2ffbdc2747c1db31da9133893619ad0402f13cbf6edc4d429ad96ca05a93`  
		Last Modified: Mon, 10 Mar 2025 22:11:16 GMT  
		Size: 434.2 MB (434154116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1c5bb71575085db1d696203bf82db1d3b81dde9cc109599a2b1a59425ff7c55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa38db58fa97e0eb40fbc16b9c3e407ac4bca203cd55fb5dce05d8c454a119c`

```dockerfile
```

-	Layers:
	-	`sha256:c795ee81e2bf4dbf92e561ac2d90dfe2b639df44c20e20c0ba7ce2227cfb6fc7`  
		Last Modified: Mon, 10 Mar 2025 22:11:05 GMT  
		Size: 6.7 MB (6654012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f1952fab76bc02371b29dc8ca3dbfbe65f25bb1e6f1a0a3aa7855fdd74cacf`  
		Last Modified: Mon, 10 Mar 2025 22:11:05 GMT  
		Size: 21.5 KB (21513 bytes)  
		MIME: application/vnd.in-toto+json
