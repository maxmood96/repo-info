## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:e83b445910c78a25a16ea730808e6b31a4093aae8dbc207e791e883c787f85b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:629609f9f3f706a8cfcf59ffa2c51d51879e3417a0673a27e1d5a420d871dd2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321511166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b12434e0695b611ebc1cb72075fd1b6f956a0f23ed56c24bb481ad6da6713`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:19:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 May 2026 16:19:50 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Fri, 08 May 2026 16:19:50 GMT
ENV PSMDB_VERSION=8.0.21-9
# Fri, 08 May 2026 16:19:50 GMT
ENV OS_VER=el9
# Fri, 08 May 2026 16:19:50 GMT
ENV FULL_PERCONA_VERSION=8.0.21-9.el9
# Fri, 08 May 2026 16:19:50 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 May 2026 16:19:50 GMT
ENV PSMDB_REPO=testing
# Fri, 08 May 2026 16:19:50 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 08 May 2026 16:19:50 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 May 2026 16:19:50 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 May 2026 16:19:50 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 May 2026 16:20:06 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Fri, 08 May 2026 16:20:06 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Fri, 08 May 2026 16:20:06 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Fri, 08 May 2026 16:20:06 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Fri, 08 May 2026 16:20:06 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 May 2026 16:20:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Fri, 08 May 2026 16:20:09 GMT
VOLUME [/data/db]
# Fri, 08 May 2026 16:20:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Fri, 08 May 2026 16:20:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Fri, 08 May 2026 16:20:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 May 2026 16:20:10 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 16:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 16:20:10 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 08 May 2026 16:20:10 GMT
USER 1001
# Fri, 08 May 2026 16:20:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a7b3ef8f213364f525b2fcb97f4cb1f23f9dd72ba6f46271b058db5345147`  
		Last Modified: Fri, 08 May 2026 16:20:41 GMT  
		Size: 8.8 MB (8836099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3bd7d635e25cf05b1f680f6496fdf574751c434fc47494ff07e0530b7884a3`  
		Last Modified: Fri, 08 May 2026 16:20:46 GMT  
		Size: 271.7 MB (271727449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e26ccd9b1b9e70743db3b38b0636b3c4e77f61860fc990fde39544ea449008`  
		Last Modified: Fri, 08 May 2026 16:20:40 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc46611fae162683f87f23d85d081da16785a82644dac8c2c9ffdba556c3ec`  
		Last Modified: Fri, 08 May 2026 16:20:40 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a90b90b595895b5fb7635549c84fbc3e25ef597303825b46d59545a3727f0e`  
		Last Modified: Fri, 08 May 2026 16:20:41 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c961678522e1e391b055b3389aaf2ba43f4be48f61c75d340d35addc06decf9`  
		Last Modified: Fri, 08 May 2026 16:20:42 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdf5c4f65632d780217ad77914ce7d799fc314259f685cbe426214a04df0d31`  
		Last Modified: Fri, 08 May 2026 16:20:39 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db183a0d0fb2fbc9ef00f3a7c72d76d83d38fabcfc680bdd3fdbb0ec1bdc70c`  
		Last Modified: Fri, 08 May 2026 16:20:42 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bc0a5a37865d4ad12a791b1a2c4faeac1917893215401a50f36dcd8f8b66c5`  
		Last Modified: Fri, 08 May 2026 16:20:43 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:3f9c6309fd86e54a581e603d0069397d3f4cc07b377dc7238b81e51241919207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b402a59fcdbd5f2a6a97f673ca0b016f0196155f8b76423210e0d463d42743bf`

```dockerfile
```

-	Layers:
	-	`sha256:995ba3d614fc3073491660c2e3025c5e6e13bab84deb7cde6c64a840fc7d473f`  
		Last Modified: Fri, 08 May 2026 16:20:40 GMT  
		Size: 32.6 KB (32575 bytes)  
		MIME: application/vnd.in-toto+json
