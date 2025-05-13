## `percona:psmdb-6.0.21`

```console
$ docker pull percona@sha256:7c44ed1a302e41101b692c96df06812b21102eaecae2731d4e64a1260ae3b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.21` - linux; amd64

```console
$ docker pull percona@sha256:08089ab27bd0130ce24fab0c95b9b107a275227ba51c928a3e7d2d7cbf06991f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254982696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3ffcb523379fda5e7b377b550b96495d2e4fdee064cfff20e39303a91f90b`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
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
COPY dir:2dc25289c3b10f6fae681d085452474bf4d133d8f435510e0e9aa64114b861ab in / 
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 22 Apr 2025 10:21:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Apr 2025 10:21:47 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 22 Apr 2025 10:21:47 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 22 Apr 2025 10:21:47 GMT
LABEL "build-date"="2025-05-13T04:42:10" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7575d7eb45eb7f545fef31ba067dfe3d8e52c4eb" "release"="1747111267"
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
	-	`sha256:719fed365262e942a8d13a9f7c6f9e87e6274c4e3ad3d0efc81666b12229084d`  
		Last Modified: Tue, 13 May 2025 05:25:18 GMT  
		Size: 39.7 MB (39714170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ddde55da83ebc0b54e635097941b2efa71a463313bf2aadc40e79791ae7258`  
		Last Modified: Tue, 13 May 2025 19:54:43 GMT  
		Size: 8.5 MB (8465488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c7440f081a8a2f5903ddd67e6e1dc0db61c97873501e1f954785cded85e6fe`  
		Last Modified: Tue, 13 May 2025 19:54:49 GMT  
		Size: 205.9 MB (205850227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb32646b5f6bea6112145f9700760cf2675b7316cbe156d31a2fd76c5e6028`  
		Last Modified: Tue, 13 May 2025 19:54:42 GMT  
		Size: 1.7 KB (1662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b9752a38154d755ba9bd33da7b4344e43ff7677fd0efdbfb45b8f53f53aa24`  
		Last Modified: Tue, 13 May 2025 19:54:42 GMT  
		Size: 4.1 KB (4069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c22526e55bfebebd0c25412753b89c4e4ddac0c126cfafca5ef0e7ccbbf1144`  
		Last Modified: Tue, 13 May 2025 19:54:42 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af089b3933db6bc3f7c6c0c69bbf83514ff524991a3c0133127a9b06632d0a2`  
		Last Modified: Tue, 13 May 2025 19:54:44 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91f905708c5ddec99b21400767c75d0c6c4836575136cc9907f83c47a228baa`  
		Last Modified: Tue, 13 May 2025 19:54:44 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662e0af24bfaceff9bed1c9d417aa39aa2c4bb30d7a58d914b0b8953f9e247f7`  
		Last Modified: Tue, 13 May 2025 19:54:44 GMT  
		Size: 4.0 KB (3957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb91fbb7e77912e63dece84d9f044acd3016a85f6141b603e992de89aeeefdc`  
		Last Modified: Tue, 13 May 2025 19:54:46 GMT  
		Size: 4.8 KB (4825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.21` - unknown; unknown

```console
$ docker pull percona@sha256:69b0e9550e4e6f46dbfda2c90a2b1c2503dc91b68b5bce66dd76aa96864434b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d247a274858261483fadd958056298bee03c49bd6d77fbe58d2c140f757d10`

```dockerfile
```

-	Layers:
	-	`sha256:31174b245891ec651f93d336e24babf2edccac07b7cec3e8498ec53a14f0089c`  
		Last Modified: Tue, 13 May 2025 19:54:42 GMT  
		Size: 33.2 KB (33241 bytes)  
		MIME: application/vnd.in-toto+json
