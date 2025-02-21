## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:ed0bc7374cee23396d06e9ac40e5ff1d6871b56fd9bd298788ff77f80720f999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:432ca25cd47169964fba009c05079d4d1d0bae4bbfc63fc3f56207da582e31c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 MB (306891538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301d4011fb2275b75663057784c43689b71d64659f3e7b78a309b2b279336155`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 Dec 2024 12:54:42 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 12:54:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 Dec 2024 12:54:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_VERSION=7.0.15-9
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=7.0.15-9.el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 Dec 2024 12:54:42 GMT
ENV PSMDB_REPO=release
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 17 Dec 2024 12:54:42 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
VOLUME [/data/db]
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 17 Dec 2024 12:54:42 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 12:54:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 12:54:42 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Dec 2024 12:54:42 GMT
USER 1001
# Tue, 17 Dec 2024 12:54:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c37909fa52f11e3d1f81e61f79a1dbc23ca04a4d3c1f496669bb97b7caf87e65`  
		Last Modified: Fri, 21 Feb 2025 19:50:24 GMT  
		Size: 100.8 MB (100797992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93b8684f26b354a87d18ed5ee04c9547d8d1a5bdf30f5d651e49cdc9c200c4e`  
		Last Modified: Fri, 21 Feb 2025 20:11:34 GMT  
		Size: 4.3 MB (4308654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510d3a9d9080861f67cb2d40d9f3eca36eded2abcf8632c7a55ed36c81337a44`  
		Last Modified: Fri, 21 Feb 2025 20:11:39 GMT  
		Size: 200.8 MB (200832499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a8ddd3ba1cb9b374978417e0508f77b98393f3b63843712249352c805b3747`  
		Last Modified: Fri, 21 Feb 2025 20:11:33 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd9a3de75185fa782e91c36c53e40c0fd94eff9d53a7ec98c0696a4fa041352`  
		Last Modified: Fri, 21 Feb 2025 20:11:33 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f55e470c53d4d304f9b70c4dea84c3cf6b97ee96df6b240b1f6fd5dd9f110a`  
		Last Modified: Fri, 21 Feb 2025 20:11:34 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4e04f1c623e6c82bb777ad473946310f321386aa92d70958019ce2fb9069fc`  
		Last Modified: Fri, 21 Feb 2025 20:11:32 GMT  
		Size: 914.5 KB (914513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5f8a5aa5e197727b3c109235d8f19e21ca36dfbb5b76d3f5122faa292ad1fa`  
		Last Modified: Fri, 21 Feb 2025 20:11:32 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91ad53fd53b3a30fd116dcd94d160d8a805f91d53752850e4fa4d583479a755`  
		Last Modified: Fri, 21 Feb 2025 20:11:35 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce495c91f200a5ebf33f6cf996452c7610c6ac6d1f9378f947723a3d1b46f01`  
		Last Modified: Fri, 21 Feb 2025 20:11:35 GMT  
		Size: 4.8 KB (4835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:b1fdf52d2b75ea42a3232e2fc0811dd829d34dbef7ee20501191c9a5dee24994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2cfff0c12fb34259315691e794b7aa1e979242c9faf7b68f151d72122b6063`

```dockerfile
```

-	Layers:
	-	`sha256:3d44f4dc95f852e418b4e91fa1f0e3aa0df5791bc5bfa28373c2eb8af980b75c`  
		Last Modified: Fri, 21 Feb 2025 20:11:33 GMT  
		Size: 32.2 KB (32215 bytes)  
		MIME: application/vnd.in-toto+json
