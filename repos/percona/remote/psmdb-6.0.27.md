## `percona:psmdb-6.0.27`

```console
$ docker pull percona@sha256:80da5d55175749b8a26df308c330abd78a106936ec9630ca91e386d007cadd5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.27` - linux; amd64

```console
$ docker pull percona@sha256:dd8faf04fc1ff5a8b3e3ab98f90c00d943e1a7b99d344878fed885c139c80bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269312490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa63fe11d8b273e23c6f2810d7ab4baaa7171b5bb61a65a6c80db457ed1ba7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:45:29 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 14 Apr 2026 20:45:29 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 14 Apr 2026 20:45:29 GMT
ENV PSMDB_VERSION=6.0.27-21
# Tue, 14 Apr 2026 20:45:29 GMT
ENV OS_VER=el9
# Tue, 14 Apr 2026 20:45:29 GMT
ENV FULL_PERCONA_VERSION=6.0.27-21.el9
# Tue, 14 Apr 2026 20:45:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 14 Apr 2026 20:45:29 GMT
ENV PSMDB_REPO=release
# Tue, 14 Apr 2026 20:45:29 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 14 Apr 2026 20:45:29 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 14 Apr 2026 20:45:29 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 14 Apr 2026 20:45:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 14 Apr 2026 20:45:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 14 Apr 2026 20:45:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 14 Apr 2026 20:45:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 14 Apr 2026 20:45:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 14 Apr 2026 20:45:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 14 Apr 2026 20:45:44 GMT
VOLUME [/data/db]
# Tue, 14 Apr 2026 20:45:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 14 Apr 2026 20:45:44 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 14 Apr 2026 20:45:44 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 14 Apr 2026 20:45:44 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:44 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 14 Apr 2026 20:45:44 GMT
USER 1001
# Tue, 14 Apr 2026 20:45:44 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4100fce197539dc16f9a2309549450daa49d35626b2fa4511536e0c28ef552e`  
		Last Modified: Tue, 14 Apr 2026 20:46:10 GMT  
		Size: 8.8 MB (8843363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de90398f247587c10d1c13116ebd0ea0953966f5517bb95ebd022232809246d2`  
		Last Modified: Tue, 14 Apr 2026 20:46:14 GMT  
		Size: 219.5 MB (219499724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9ccd9ef3799c1e13c7c3bbd5ec5b98e5a32136fe0f6888049d26583336babf`  
		Last Modified: Tue, 14 Apr 2026 20:46:10 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4c1d2730455546f2e72c2170713bed1051ff5a0b7d851ae7e2d7de1a9ea21e`  
		Last Modified: Tue, 14 Apr 2026 20:46:10 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaad1a9e68ef7bb6eb89c8b6f3cda0fd8e569d9de87e05d75d9434d6c356376`  
		Last Modified: Tue, 14 Apr 2026 20:46:11 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2d57bb21730c6554cded1e58f46cef352c1fe9f31bcdbe8dc6f239699d1795`  
		Last Modified: Tue, 14 Apr 2026 20:46:11 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dde5819240c89fa0b2d9b2d820a9a0c63e75e0f6937882fa3fd55857e3bb4df`  
		Last Modified: Tue, 14 Apr 2026 20:46:11 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d538f6590c7288ff980baf6c57dd593921f043e927748735cd874b53e0ef4c0`  
		Last Modified: Tue, 14 Apr 2026 20:46:12 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c8992ad226cf8013c4509c9dd96832dafff1006afc7489b977b7fef992d2c4`  
		Last Modified: Tue, 14 Apr 2026 20:46:13 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.27` - unknown; unknown

```console
$ docker pull percona@sha256:cd10b71160fb7c056ce0341d72ede0ee2400825fbb272aac5ff7d0ac1f3a36c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3a28fe97bf1e727db4adb8a72785d173ebd27bff8d2aa3c8aed1c3bbd8c2ef`

```dockerfile
```

-	Layers:
	-	`sha256:9fb5c3a8e8dce6b9de766eb47a65fe27f40e173d42ffe3b666c57bd9667bcd60`  
		Last Modified: Tue, 14 Apr 2026 20:46:10 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json
