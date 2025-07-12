## `percona:psmdb-6.0.24`

```console
$ docker pull percona@sha256:471a867eede290d2ef926516dda4cd6f3a45fd1a4134b9219eb3bdf56b812675
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.24` - linux; amd64

```console
$ docker pull percona@sha256:afc4cb0a72829e1dc4660f60e9faa8ce645c3092a804d6e603c6467a88165603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254128962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee715c58baf8a12a38abed0dd9934e01351587c3373c77fdd4655a2c8716896`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL url="https://www.redhat.com"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 07 Jul 2025 10:50:23 GMT
ENV container oci
# Mon, 07 Jul 2025 10:50:23 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 10:50:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Mon, 07 Jul 2025 10:50:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 07 Jul 2025 10:50:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_VERSION=6.0.24-19
# Mon, 07 Jul 2025 10:50:23 GMT
ENV OS_VER=el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV FULL_PERCONA_VERSION=6.0.24-19.el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_REPO=release
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 07 Jul 2025 10:50:23 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV GOSU_VERSION=1.11
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
VOLUME [/data/db]
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 07 Jul 2025 10:50:23 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Jul 2025 10:50:23 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 07 Jul 2025 10:50:23 GMT
USER 1001
# Mon, 07 Jul 2025 10:50:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64953ab748f36a795befd74abf4063061fe05df8cd7f9999930525c106f015a7`  
		Last Modified: Fri, 11 Jul 2025 23:34:01 GMT  
		Size: 8.5 MB (8485659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556b6b542ac0853538d9259203188491885ea5bfb913063c03a2beea0b7c791b`  
		Last Modified: Sat, 12 Jul 2025 02:13:17 GMT  
		Size: 205.0 MB (205033683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1908508d72ec5abce27df3c5367878b1e2847ab6deb35d03b13197979db6202b`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722eed0ff7f5cf00d586e41fd739ba239a5e982fae6e27061ff43040ff41ed02`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b986a3da8d36529e64e4df5fa562c1d00a289adf449f519a937b9890273cf72`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ea2a25f53065ba9c10482fb46e664fe58b5857ade5dc331cf1f710400c3e06`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c5b5b057ba9244e8a57df6a21c6ce68c318559a76086e92869288d9896fb8`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6982a8cfde517acb45fe3d8dcd6e647f591b6e1349ea5b697e82c9494329a7a3`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349550007b733877149b50f499ce674e67d247036874e319f5fee57c796a678b`  
		Last Modified: Fri, 11 Jul 2025 23:34:00 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.24` - unknown; unknown

```console
$ docker pull percona@sha256:9d15da33982c7144889b97a7156c1eec82c3418a005a00db72797e4e87df4f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d47d559c1172e2e879f1cc77cfc686b3cbd62f85336057355f099ab8ed7835b`

```dockerfile
```

-	Layers:
	-	`sha256:a0f159fbed0c3707fc619f4e715539e8e37c0c8a91f4b8fb88b0d1af50bdcb63`  
		Last Modified: Sat, 12 Jul 2025 02:10:30 GMT  
		Size: 32.7 KB (32657 bytes)  
		MIME: application/vnd.in-toto+json
