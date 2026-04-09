## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:6d1e73e6d6547c4e5b8c36642e468e6022382b36f869d2fcd02b4ae02f040e32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:cec963b26127c3f1b5146bd861ec5fbc91cfd6247d70c22456d817c67ae3a7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320159910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0101eb2160f7382c209ea943b6534c689f8855ad2c73e37aba139d36598224`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 08 Apr 2026 17:23:56 GMT
ENV PSMDB_VERSION=8.0.20-8
# Wed, 08 Apr 2026 17:23:56 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:56 GMT
ENV FULL_PERCONA_VERSION=8.0.20-8.el9
# Wed, 08 Apr 2026 17:23:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Apr 2026 17:23:56 GMT
ENV PSMDB_REPO=testing
# Wed, 08 Apr 2026 17:23:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 08 Apr 2026 17:23:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:56 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 08 Apr 2026 17:24:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 08 Apr 2026 17:24:15 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Apr 2026 17:24:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 08 Apr 2026 17:24:16 GMT
VOLUME [/data/db]
# Wed, 08 Apr 2026 17:24:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:17 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:17 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 08 Apr 2026 17:24:17 GMT
USER 1001
# Wed, 08 Apr 2026 17:24:17 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eb2a02acb531c8ccab94330ecf99d49de21aeb66dc5bf4ee7a1c13b34676cb`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 8.8 MB (8844023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c726606b66c36acd816bfe14327be599d1e048f759883d3c9d96e99dbc43591`  
		Last Modified: Wed, 08 Apr 2026 17:25:00 GMT  
		Size: 270.4 MB (270380402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe96b8263b38aac6e470f3026ce6aaecabe16e7b43ce3cf88263fc120b82632c`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8828acc245febde2c1ff06a0df54b79029d0fe5df80ec71e9562bdc25e8e5`  
		Last Modified: Wed, 08 Apr 2026 17:24:54 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad06daa8c97caf7be6bbd123d50139d2d31a3a5463642dc933ba47776cb5bf5`  
		Last Modified: Wed, 08 Apr 2026 17:24:55 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af1f7ed81ae0ae7d02ff69bfcb25461587c0ef0e7adfd1029792cbc91d19765`  
		Last Modified: Wed, 08 Apr 2026 17:24:55 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325bcd62172d458666c766cf6606b57eb83b276d912ce7330cc1570f0a17ac05`  
		Last Modified: Wed, 08 Apr 2026 17:24:56 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d9ecbd9953ba7f6499a1497e5dde2427854eef2c7cce6dbf30e16594570d`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab225c2f86027799b49c036cb2c178ce3916eb7c34e92bd81b4f9055ee47584e`  
		Last Modified: Wed, 08 Apr 2026 17:24:57 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:bfe8504b8db52d01bf9696c974af0ae53ad4674ddcb073c08f00dd057fdbc963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f234dac9c14aa0be7056143994ef9d9ecf52df46b1364084bf6df56c3ac5adff`

```dockerfile
```

-	Layers:
	-	`sha256:43eb450a871f5640c475a4ccac22ff7bd4d7c7e9211fbc731458fabbbca4a287`  
		Last Modified: Wed, 08 Apr 2026 17:24:53 GMT  
		Size: 32.6 KB (32575 bytes)  
		MIME: application/vnd.in-toto+json
