## `percona:psmdb-6.0.19`

```console
$ docker pull percona@sha256:32bd70e1b3219cb51826be58298ffb217915e2de44a04e80e62e73d65340f99e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.19` - linux; amd64

```console
$ docker pull percona@sha256:327d5ef8a02f21071fc868ce0af9264976b8b11cb24bbf911c3da13e7d11f715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295440935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f76bae000213a5f27af070e9e4a019b3af901911684a572d41b06d505d388e`
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
ENV PSMDB_VERSION=6.0.19-16
# Tue, 17 Dec 2024 12:54:42 GMT
ENV OS_VER=el8
# Tue, 17 Dec 2024 12:54:42 GMT
ENV FULL_PERCONA_VERSION=6.0.19-16.el8
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
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y update openssh;     dnf -y update bind-export-libs;     dnf -y update glibc;     dnf -y update libgcrypt;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
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
	-	`sha256:3b6f0a53c915c6b97578c3b6958123190d7abeb100a9218d8b40d6b1118b8a42`  
		Last Modified: Tue, 15 Apr 2025 21:51:29 GMT  
		Size: 100.8 MB (100819115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa50f4eda37caf090ddae6cea7b3ff7e68f7640f199e1b32cb576bf7c56984b`  
		Last Modified: Tue, 15 Apr 2025 21:56:28 GMT  
		Size: 4.3 MB (4316943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46eebb363533df5f33840eb7f5b55ba8649f7d901d4501b612c09d6387d0f773`  
		Last Modified: Tue, 15 Apr 2025 21:56:31 GMT  
		Size: 189.4 MB (189352487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e04cf82f90890eeee543b36f05436ba118fbb3e0abd9c8da321efcb1ac3974b`  
		Last Modified: Tue, 15 Apr 2025 21:56:28 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0251039ba3820b120d796a8a17b2e2d93fbcf7a07a7e0c2418e508e4e8772f6e`  
		Last Modified: Tue, 15 Apr 2025 21:56:28 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aecf14f528b6b0012daa8a8cfb8de1275e0d5611f3e0f61295d329f561ffe42`  
		Last Modified: Tue, 15 Apr 2025 21:56:29 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4a41a5f4856cf1db9f3ad7fb4f5dd66ab1395da9a47bff18089a7e13fbeaa0`  
		Last Modified: Tue, 15 Apr 2025 21:56:29 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38a60ad5f8e7ef43d256e1f0142b77bb26073f3c2ecfd19fe3c4994be0d7524`  
		Last Modified: Tue, 15 Apr 2025 21:56:29 GMT  
		Size: 13.2 KB (13206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa0be6aefe50a9d0a8971a914eb7b31e1308830054aeffa9e000bf62f49a212`  
		Last Modified: Tue, 15 Apr 2025 21:56:30 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62edf80279ae5062a8dfea020abf305cb9a991acb1b368915e5eab008e96960f`  
		Last Modified: Tue, 15 Apr 2025 21:56:30 GMT  
		Size: 4.8 KB (4833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.19` - unknown; unknown

```console
$ docker pull percona@sha256:58125348def0e49ecda8c3ea1474aa08a160d14ce7dfcb67e7555b8a4f18d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1638d8c2de46d547dd3e0124eae40cb66e65c505c9e75d89ab13ef15a9fb504`

```dockerfile
```

-	Layers:
	-	`sha256:ccd2c173d0a9392348559d5972bb8ff651a5d002dbcfdbd09d651562ac7e1459`  
		Last Modified: Tue, 15 Apr 2025 21:56:28 GMT  
		Size: 32.2 KB (32227 bytes)  
		MIME: application/vnd.in-toto+json
