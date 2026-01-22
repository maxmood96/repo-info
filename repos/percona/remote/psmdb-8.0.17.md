## `percona:psmdb-8.0.17`

```console
$ docker pull percona@sha256:bec376cac72d2ae4e40fde70bd32605bff582801eec1fcc9e196fbcfdc23120c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.17` - linux; amd64

```console
$ docker pull percona@sha256:24af3d914dbb7dfd40503209076ca65560d4b992e14080449de81d4e7a4bc319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307619191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe33f90ffa56798445e53718edcfcfcb3fa9bfb048ec9b93143e8c4040fa2ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:13:29 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 20 Jan 2026 19:13:29 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 20 Jan 2026 19:13:29 GMT
ENV PSMDB_VERSION=8.0.17-6
# Tue, 20 Jan 2026 19:13:29 GMT
ENV OS_VER=el9
# Tue, 20 Jan 2026 19:13:29 GMT
ENV FULL_PERCONA_VERSION=8.0.17-6.el9
# Tue, 20 Jan 2026 19:13:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 20 Jan 2026 19:13:29 GMT
ENV PSMDB_REPO=testing
# Tue, 20 Jan 2026 19:13:29 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 20 Jan 2026 19:13:29 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 20 Jan 2026 19:13:29 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 20 Jan 2026 19:13:29 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 20 Jan 2026 19:13:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 20 Jan 2026 19:13:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 20 Jan 2026 19:13:46 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 20 Jan 2026 19:13:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 20 Jan 2026 19:13:46 GMT
ENV GOSU_VERSION=1.11
# Tue, 20 Jan 2026 19:13:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 20 Jan 2026 19:13:48 GMT
VOLUME [/data/db]
# Tue, 20 Jan 2026 19:13:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 20 Jan 2026 19:13:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 20 Jan 2026 19:13:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 20 Jan 2026 19:13:49 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jan 2026 19:13:49 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 20 Jan 2026 19:13:49 GMT
USER 1001
# Tue, 20 Jan 2026 19:13:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:34 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff95d0217c685aa52f18dc51d6f1d9b22b024a088e844951e594a01f68e66565`  
		Last Modified: Tue, 20 Jan 2026 19:14:19 GMT  
		Size: 8.8 MB (8844591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf5687b6a34f513253832592347860f377eb583777cc7f6359e4a15e6c84b7f`  
		Last Modified: Tue, 20 Jan 2026 19:38:35 GMT  
		Size: 257.8 MB (257788555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bed49d50316e9650cdd9225554389a21ca4a87fae6bc9ca7ef41d752f65dc14`  
		Last Modified: Tue, 20 Jan 2026 19:14:19 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699f9e0f0178f6053d87445d6e08c1eed17bdcd1fab06846b4b36e3874a3c5c`  
		Last Modified: Tue, 20 Jan 2026 19:14:20 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412fd060834d3e362e4ef53baaa3e3e1b241b27ab1e1a7428f98f1a678abaa02`  
		Last Modified: Tue, 20 Jan 2026 21:14:39 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67389135dba6f3c04605ffd619ab8f799f998161565b89ad18b93f56ebf42ab3`  
		Last Modified: Tue, 20 Jan 2026 19:14:32 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbf9661be5d4407ad1fe7fb0df4f3b23a151e0eab8373c12e7dd3bdb18a1490`  
		Last Modified: Tue, 20 Jan 2026 19:14:21 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6643fc91eff699a6addcfd1d22da4536cbcf817f461c715e70bcc9766576762`  
		Last Modified: Tue, 20 Jan 2026 19:14:21 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16964c0734baaa6e2fc2ce01ad13d474ed7f80eb6364973d26143e24dd02dbc0`  
		Last Modified: Tue, 20 Jan 2026 19:14:22 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.17` - unknown; unknown

```console
$ docker pull percona@sha256:6ae2bcf670d08fdc881f6287a9d5188e62aaeb9ec11ef92712a5fbb5afb87e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb76d75e58439740b90f2a3eb986dcd5374cb99e580642e0e9a20f0179818c34`

```dockerfile
```

-	Layers:
	-	`sha256:f9ff799522449c1ec36e0d3f955d71816bb354df5034648b68cb88490359033a`  
		Last Modified: Tue, 20 Jan 2026 19:14:19 GMT  
		Size: 32.6 KB (32575 bytes)  
		MIME: application/vnd.in-toto+json
