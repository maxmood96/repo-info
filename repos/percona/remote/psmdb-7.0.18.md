## `percona:psmdb-7.0.18`

```console
$ docker pull percona@sha256:2d6118f4d11c9a85dda1c1e047771a7098567623e97abceb6d3de73b5ab8f8a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.18` - linux; amd64

```console
$ docker pull percona@sha256:16fc69b089978f60e9f9f8145521fed804232780ef2f27953025823af8c2713a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269218795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0058f15d7daa8f591015736a7780a16df1b14d2031d06ead85ffdb5db6c85108`
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
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 07 Jul 2025 10:50:23 GMT
ENV PSMDB_VERSION=7.0.18-11
# Mon, 07 Jul 2025 10:50:23 GMT
ENV OS_VER=el9
# Mon, 07 Jul 2025 10:50:23 GMT
ENV FULL_PERCONA_VERSION=7.0.18-11.el9
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
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
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
	-	`sha256:0b0da90dfebcb299ff9cb89d2d0d8cd2e783ca36f9b8a1cb066b58d20cf0801c`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 8.5 MB (8481289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27177bb509eb98f62fcaeafb5beb20b3f624767723ae6d7101cf98460984b187`  
		Last Modified: Sat, 12 Jul 2025 02:15:24 GMT  
		Size: 220.1 MB (220127878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0577c4a7d4d99b2c2871b10d0fc4b7d392760e1b70fcbcc94594351c0c23fefe`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57ed847744e4667f2093fb8f0918c22c70467690f9640ab7877182e5b2ff116`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000745fad3d0691e85ec397a5b3cf648806db686489f123b2998047cc3e713ec`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b0844664c4aef9027e8e8ef8002d2840cca068e6aa113385b582f668dd0450`  
		Last Modified: Fri, 11 Jul 2025 23:33:56 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b15d666a91ba2d271f4247cf97c7db8c7340b9639e0561b3efd7137372665`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccfa7a968cce8cf3e95c82293dd0594b9d928317a0e5c59556234d877a78cb0`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cab42d3c28e985500340a0643faae66ce72ff9dbcb15cd41d211ae7fb0a5a9`  
		Last Modified: Fri, 11 Jul 2025 23:33:55 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.18` - unknown; unknown

```console
$ docker pull percona@sha256:5b431c121af908ea25038fac225206889d8f48a6e00b25cbd526df859b021dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8c213b3ffd1a2b8744869d0036754c3f259945f7ef0490b1fe7aedcf2f2296`

```dockerfile
```

-	Layers:
	-	`sha256:b6775a52539eb9d6de092ebd7ed7caa559bdce5bf719c2c4bad8b7048f33e4e6`  
		Last Modified: Sat, 12 Jul 2025 02:10:36 GMT  
		Size: 32.2 KB (32166 bytes)  
		MIME: application/vnd.in-toto+json
