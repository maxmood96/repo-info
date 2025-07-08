## `percona:psmdb-7.0.18`

```console
$ docker pull percona@sha256:65f95144aeb134313b5303f3a0523070e1b23b095ae09318523d04382beedf33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.18` - linux; amd64

```console
$ docker pull percona@sha256:84207dbbad093a1d0d38d7f88271441caede016ed7a98c5691e91601f8f6885c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269195892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214ff393a558d95bbfc21b952d41ebfea0d27abf34a83c1cd7442b3469f3c997`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL url="https://www.redhat.com"
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 30 Jun 2025 12:32:21 GMT
LABEL io.openshift.expose-services=""
# Mon, 30 Jun 2025 12:32:22 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 30 Jun 2025 12:32:22 GMT
ENV container oci
# Mon, 30 Jun 2025 12:32:22 GMT
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Mon, 30 Jun 2025 12:32:23 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Mon, 30 Jun 2025 12:32:23 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 12:32:23 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Mon, 30 Jun 2025 12:32:24 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d2f22d3d79307186bca7686c731cfc7913f710edb40e219eb048a894b90e47`  
		Last Modified: Mon, 07 Jul 2025 20:49:46 GMT  
		Size: 8.5 MB (8470627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a691da08e1fcdfab51f8f85e0f143de93965c8b6f685ed4cfb8079b2a011ef7`  
		Last Modified: Mon, 07 Jul 2025 23:10:44 GMT  
		Size: 220.1 MB (220121601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616ea7e627d85eb3763317a057c755f5d07e295e255d0c43a7f78305aea814c4`  
		Last Modified: Mon, 07 Jul 2025 20:49:46 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d860732246ec48a46d52de382fc61247e1317b855a9ec32eb8ef14226bd4d855`  
		Last Modified: Mon, 07 Jul 2025 20:49:45 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0885069877d694edf3898d1eb65128f076809e7977830e44e45182a35ddc79d0`  
		Last Modified: Mon, 07 Jul 2025 20:49:45 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c74be9e8deefd4d1027ae5c6d34d91b9820d8a377e92a9352d44eb1263081`  
		Last Modified: Mon, 07 Jul 2025 20:49:46 GMT  
		Size: 914.5 KB (914515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb734ad4d3a8b6fb5d1a5cee95af248d41e790e6f4e65bf7aa8d6447f4af77`  
		Last Modified: Mon, 07 Jul 2025 20:49:45 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61f34b82f047aff251034aed0f645636cbc9f68e8e30ed48ccdccd6938310cc`  
		Last Modified: Mon, 07 Jul 2025 20:49:45 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf53ec28540eff857d76de8413e776cd8e6e593ea5c9f46cd22536f3afcdc1a`  
		Last Modified: Mon, 07 Jul 2025 20:49:45 GMT  
		Size: 4.8 KB (4849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.18` - unknown; unknown

```console
$ docker pull percona@sha256:5cd22d60ad7d68b3ad89ae37ab9a009cc2e4794589c38dc8aafd741a21b193ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d090736853417f6e5dd45ce6a4e40ce726948e8a7488d3180b3f717de3f295`

```dockerfile
```

-	Layers:
	-	`sha256:072845eca48d02f8cd62086324c5a9ee439efdfec4bb415546de1c5319c12e54`  
		Last Modified: Mon, 07 Jul 2025 23:10:25 GMT  
		Size: 32.2 KB (32167 bytes)  
		MIME: application/vnd.in-toto+json
