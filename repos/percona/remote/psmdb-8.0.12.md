## `percona:psmdb-8.0.12`

```console
$ docker pull percona@sha256:39dbc583edec6a58b82b9f23b47607dfee02a72ec529e9611518cc0d7e9655cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.12` - linux; amd64

```console
$ docker pull percona@sha256:15b45b89f3c38fc143cc28efb93091f67ed7040334597d1d6277503f9cd506a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291774187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6798f738d5c77d1946ea113979f37b63d7d48b9549e180315bd2099eec688d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 13:56:56 GMT
ENV container oci
# Mon, 06 Oct 2025 13:56:56 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=8.0.12-4
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=8.0.12-4.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=testing
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfc5ced32602c6cce2466c511555dc95d459a6930a07c7707a7a82592d1cf1c`  
		Last Modified: Thu, 16 Oct 2025 19:26:48 GMT  
		Size: 8.4 MB (8391239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99beb58a3909878b71b0f95234b6e94a08d7fee1c9ec7402480b31daa22f3063`  
		Last Modified: Thu, 16 Oct 2025 23:11:25 GMT  
		Size: 242.8 MB (242776578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b69c7f9d06d0486a4b6cdc7e93e3cdeba0af1e95720f0f281a8dd67cab69a6a`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a1a21176a09e883b28dc2a41a895771321e9d6be5d492444a714039bd112a`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3e70ce7edd347f3b06710259fe97fd71e51c58df462ef973f8c3ba86ffca99`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c0ffa3aedc10a930e4f4b765e6a23a816fb410b6d2990da0bf45bd833fad61`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 914.5 KB (914519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2035a26116fa6ca7dca74fb49e50f1b7b140561c098e1e2936a06c9dda398`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef752afd6582565a403764e5a84b7d800aa561aa76056fe612b43d2ecdb1859`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9103b540ae4e093627b0832735a8cd7802d507cea2e3e1c56c5548f7f40a7e56`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.12` - unknown; unknown

```console
$ docker pull percona@sha256:ad37ac0aa4f8e9f50e6170305a27cecac5d6cb3b44f4a1852bbf118b5fc7e1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7888ad41be1f3e9da720d808fbdbb783a9d5fcab759f20c9266dccc53a3d5cfb`

```dockerfile
```

-	Layers:
	-	`sha256:a8aea2cac4e4c9b88c73fe821f546808c06ada9439d6ad9f3201f0dc1ae45746`  
		Last Modified: Thu, 16 Oct 2025 23:10:49 GMT  
		Size: 32.6 KB (32618 bytes)  
		MIME: application/vnd.in-toto+json
