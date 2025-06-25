## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:9569572e37ab3a227e219950851ebbd029547d572699cc3d8ba53e9952b20cc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:b43a3ed5e083731063eac92dc03410a36155099a6a2f08fbb18e4abac9341848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254039844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de300d6b8971459e58e1cbf8f9d251605918edc716daf8b5907b7f3d35eb5d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL url="https://www.redhat.com"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 22 Apr 2025 10:21:47 GMT
ENV container oci
# Tue, 22 Apr 2025 10:21:47 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 22 Apr 2025 10:21:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_VERSION=6.0.21-18
# Tue, 22 Apr 2025 10:21:47 GMT
ENV OS_VER=el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV FULL_PERCONA_VERSION=6.0.21-18.el9
# Tue, 22 Apr 2025 10:21:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 22 Apr 2025 10:21:47 GMT
ENV PSMDB_REPO=release
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 22 Apr 2025 10:21:47 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     curl -Lf -o /tmp/numactl.rpm https://yum.oracle.com/repo/OracleLinux/OL9/baseos/latest/x86_64/getPackage/numactl-2.0.16-1.el9.x86_64.rpm;     rpmkeys --checksig /tmp/numactl.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rpm -i /tmp/numactl.rpm;     rm -rf /tmp/numactl.rpm /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV GOSU_VERSION=1.11
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
VOLUME [/data/db]
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 22 Apr 2025 10:21:47 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 22 Apr 2025 10:21:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Apr 2025 10:21:47 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 22 Apr 2025 10:21:47 GMT
USER 1001
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87504026691c210528e254b5fe78bf3e74609134b90d1513d9577f2bf0017f8`  
		Last Modified: Wed, 25 Jun 2025 20:10:55 GMT  
		Size: 8.5 MB (8476225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091d50ca8d8701ef5efa5338422538d9b2ceff08c75be37e2bfbb82ca6ad43b3`  
		Last Modified: Wed, 25 Jun 2025 20:11:10 GMT  
		Size: 205.0 MB (204960132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f30e9d3009a739fa575b37aa16e58350dc8bb1b28f86ccff1bc2b702d0e16ec`  
		Last Modified: Wed, 25 Jun 2025 18:08:56 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c30731d11151484a7c9b1a6c717324a4f9693f493a7b4496b198b5603680d2`  
		Last Modified: Wed, 25 Jun 2025 18:08:59 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95f5d10c5097a9b95c4fdf7fbee54182f160041c3b0305e835cabff518f8394`  
		Last Modified: Wed, 25 Jun 2025 18:09:02 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdb64b57512aeeb3adf0ea2667af39e9803f57ac43c680c1f9d905f35ea1d7b`  
		Last Modified: Wed, 25 Jun 2025 18:09:10 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8af55231b93bebd05562a62db0ef8bfa34e0b0870bca6d9e9e9d14e18741bdf`  
		Last Modified: Wed, 25 Jun 2025 18:09:14 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c8cbe5586e72115c1dd458db55d4535848a5bc88b782160e4356e3dcce7f10`  
		Last Modified: Wed, 25 Jun 2025 18:09:18 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c429957f72756e7057da810e74522dbe292b1c3ac70cc485bc47c0a3ad3d1`  
		Last Modified: Wed, 25 Jun 2025 18:09:24 GMT  
		Size: 4.8 KB (4826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:53182ff463f6117684cfe7d91a6dc57dc356a61d85ad38c83d81ccdacbfda0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aa3331997cb1794df02ae638b9c9d34275ce98be4fd6e51c519ca4e5976820`

```dockerfile
```

-	Layers:
	-	`sha256:25c020275cb4dec84e2870356cacee9b39312a87732e1d9d383f4f7a2fd1c3b9`  
		Last Modified: Wed, 25 Jun 2025 20:10:49 GMT  
		Size: 33.2 KB (33241 bytes)  
		MIME: application/vnd.in-toto+json
