## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:b8bb4997686f5c77541ad98cfcaec5cc440c5ec7519b81577993305beca9ae59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:ec5f008769abbcf2ffcc1145c8679c5c505168cea4bb6179779ce54374731140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320191583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f92805a77ee637203f79d1bde73254b16733c963dd3cbe53add05704c1c5ca`
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
# Tue, 14 Apr 2026 20:45:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 14 Apr 2026 20:45:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 14 Apr 2026 20:45:04 GMT
ENV PSMDB_VERSION=8.0.20-8
# Tue, 14 Apr 2026 20:45:04 GMT
ENV OS_VER=el9
# Tue, 14 Apr 2026 20:45:04 GMT
ENV FULL_PERCONA_VERSION=8.0.20-8.el9
# Tue, 14 Apr 2026 20:45:04 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 14 Apr 2026 20:45:04 GMT
ENV PSMDB_REPO=testing
# Tue, 14 Apr 2026 20:45:04 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 14 Apr 2026 20:45:04 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 14 Apr 2026 20:45:04 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 14 Apr 2026 20:45:04 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 14 Apr 2026 20:45:21 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 14 Apr 2026 20:45:21 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 14 Apr 2026 20:45:21 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 14 Apr 2026 20:45:21 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 14 Apr 2026 20:45:21 GMT
ENV GOSU_VERSION=1.11
# Tue, 14 Apr 2026 20:45:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 14 Apr 2026 20:45:23 GMT
VOLUME [/data/db]
# Tue, 14 Apr 2026 20:45:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 14 Apr 2026 20:45:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 14 Apr 2026 20:45:24 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 14 Apr 2026 20:45:24 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:24 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 14 Apr 2026 20:45:24 GMT
USER 1001
# Tue, 14 Apr 2026 20:45:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeeb8547d60607e5f9f8de658b46c5e6d62704fa3865541b55af575df42686f`  
		Last Modified: Tue, 14 Apr 2026 20:45:56 GMT  
		Size: 8.8 MB (8839866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c383c331805cfcb2c00c885f9745071b3ff6b647701313742b904ef9efe9aeb1`  
		Last Modified: Tue, 14 Apr 2026 20:46:01 GMT  
		Size: 270.4 MB (270382321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7d57956e46014aba57d0e0b810ab218704a8be0d586d42829e498947492c30`  
		Last Modified: Tue, 14 Apr 2026 20:45:55 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7376fa08af57274ffe5206e061f25119f45dbf02009d0f6ddf5b3846ba023ce`  
		Last Modified: Tue, 14 Apr 2026 20:45:56 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5157fb9efb4f4f61de1d910294e24603f0a728cd11b5b4b9e053fd0715fea2`  
		Last Modified: Tue, 14 Apr 2026 20:45:57 GMT  
		Size: 10.6 KB (10574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc16bab382401c3a8b82b52af09cfd2685f3c5b5dd75a8f4bdb2206772426b41`  
		Last Modified: Tue, 14 Apr 2026 20:45:57 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10dbec99367465d5db459b45a559abd9fed163d7807e6b1f1c7460996a1750`  
		Last Modified: Tue, 14 Apr 2026 20:45:58 GMT  
		Size: 13.2 KB (13203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d609d857c561e909e2a56ba370d34010f6e30963f54a431ac99587d5adc2cd37`  
		Last Modified: Tue, 14 Apr 2026 20:45:58 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347680a51c7f838aab3b6d1e4c8d8e5f86f8d3f0dd49ecedee792759d8664714`  
		Last Modified: Tue, 14 Apr 2026 20:45:58 GMT  
		Size: 4.8 KB (4841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:94360051dbaaa05a95de45480c621106cc71c1f43cea9630551d5951ca08085a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881ded23c6b2f2e7812126b4c2774d039e68e91020b9b73dbfd3c45f107a42b`

```dockerfile
```

-	Layers:
	-	`sha256:7a950a050240c9b2baca8a6d597f48c4797e4725bb684c2d29bd1af11c161329`  
		Last Modified: Tue, 14 Apr 2026 20:45:56 GMT  
		Size: 32.6 KB (32574 bytes)  
		MIME: application/vnd.in-toto+json
