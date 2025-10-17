## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:f7637802f11bfcf83fe03b586a4527387b351eb1796f588ca1cf18d395d29e72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:501d25e60229b7a7af73925fc42b79b8077ca05c2910c235beb14ac99dcac3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254060438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4065bb0ad92a4656e2f1cf498edd5cb35e0cfe844edd022c034d6287a6e31c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:26:55 GMT
ENV container oci
# Fri, 01 Aug 2025 11:26:55 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 01 Aug 2025 11:26:55 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_VERSION=6.0.25-20
# Fri, 01 Aug 2025 11:26:55 GMT
ENV OS_VER=el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_REPO=release
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 01 Aug 2025 11:26:55 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
VOLUME [/data/db]
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 01 Aug 2025 11:26:55 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Aug 2025 11:26:55 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 01 Aug 2025 11:26:55 GMT
USER 1001
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0971d255497469d093a54a7fbf3f6fb35ec433649ae1f5a0b160320b9a3290d`  
		Last Modified: Thu, 16 Oct 2025 19:27:17 GMT  
		Size: 8.4 MB (8395932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1712c28a52083944a7de810e8cdf8071d0950d70ddb15e35c7ce2739d50687f1`  
		Last Modified: Thu, 16 Oct 2025 23:11:07 GMT  
		Size: 205.1 MB (205058137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acbf9600f259ea91dccba2ca5cd69033af8df6301983a1f73e646bcb8a692e5`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba96ac3ce7b0f2c521202300b8a80541ebab4af82d7ebb27e988ee9a51265114`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c552db3238aa4c5b05a922fb6c541f6876b5984efc7de1924db3ba777f13d5e5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f22e3806828979064da80e3bbddb9b7753fec5f751b845788720aec9526a190`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f3d23fbde43f9d4ff9b120bf967cff670b2fc9c59fdc69992a0a9ed9651a61`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ccf9b40d441f1e41d395ec5d0e5eb358b5ad4fb2316edb99cc4903fd151a8c`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c00ce65c4e1a6fe41d8e2ebe30a85479401387b0b7191c2461e8f02b207a04`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:04759dc7bf69c8c5bef17c523b2705865b678429fca117435efb03fd79628ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3624cfb65bcc3fffb2e901e33b9bfb046ea56f6b24d26539a7a22d8d482ea0`

```dockerfile
```

-	Layers:
	-	`sha256:86e55870ac8106299bdf4863ad21ac10bb49f2ea6c912c02777cd47a14933b9f`  
		Last Modified: Thu, 16 Oct 2025 23:10:37 GMT  
		Size: 32.8 KB (32821 bytes)  
		MIME: application/vnd.in-toto+json
