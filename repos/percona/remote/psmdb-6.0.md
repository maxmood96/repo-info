## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:ac2eb9eac7cc1b3e877b342434c4b6cdfc63f667e6bcdf8750e4e66ad1e2614c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:86148f392c26483cba5cd3205cc403ef8b185b646b658d338e77c9c160206ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254134473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcfa151a60bf4e88dcaa2fbfc0df3722690584cc2b8d684e0b2f3592a27aa4b`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
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
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05ff4ef99fb2a8b100fb348e16b103f7a259d758b5776a0112cd66d2caad658`  
		Last Modified: Wed, 13 Aug 2025 23:02:05 GMT  
		Size: 8.5 MB (8482456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0fdbc8979cfb9982a6611eb02afbc39d89faaa79e55377e4ba8eddf950e4a`  
		Last Modified: Thu, 14 Aug 2025 02:14:56 GMT  
		Size: 205.0 MB (205047875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ee8de7cc7c2232ab820ff27a4af281daf0126c7e71984f83da7eb176757d05`  
		Last Modified: Wed, 13 Aug 2025 23:02:03 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d14581c648863ec55f2cb325fafa857d45746445c9bbcc7e9a9497f632d7f13`  
		Last Modified: Wed, 13 Aug 2025 23:02:04 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf7f21a18a68ae8ddafcc0e684647d6aeb3fef932b616c86e5a3672d2f8798e`  
		Last Modified: Wed, 13 Aug 2025 23:02:04 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f709e24ae6772bc9c7acc562e6cceee9cb29cbb85436a4fa7c65d9287fe54d`  
		Last Modified: Wed, 13 Aug 2025 23:02:05 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58234d171a7f90be5fae1018736f7f4aa7b99d7535cb13857441bbf0bdc30fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:06 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8ef781d767583171a7182fe27c0517f395923d21c3b5884e1f79f4e0b51ce0`  
		Last Modified: Wed, 13 Aug 2025 23:02:06 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd19b805240093a9da9cf495ef212ae3f4836fcad958723a96175122a4f3fe96`  
		Last Modified: Wed, 13 Aug 2025 23:02:06 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:506f2038aa38a61b4d8fb4721ed49294f9c32a77dafcebfdd0eb870bf17085cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e749e2cac48af3fef00c74e2db538a25d74a9826dbe9f2d8ab513fbcbe8ddfb6`

```dockerfile
```

-	Layers:
	-	`sha256:b673c28df6353d47b06df3cb5eb0203916acadb876200ed86d8cc02b4941178b`  
		Last Modified: Thu, 14 Aug 2025 02:10:26 GMT  
		Size: 32.8 KB (32761 bytes)  
		MIME: application/vnd.in-toto+json
