## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:20b711d62d3fb18d7ddec5625f596a8be62af2f59f4d5d190c49dd7a1cf11ca6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:bb722691f869a5edced0db0c6556c3269839af5ccc0a1b302c4739d93b695f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295379976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ce37f7363b79f4d201d1a9eef7d0575f0c5841a510e768aac8d2f3827af73`
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
	-	`sha256:e198ceced898a56d9a661e15048ed0ee31744f30be88f061bcf4455493edda67`  
		Last Modified: Fri, 14 Mar 2025 19:00:17 GMT  
		Size: 100.8 MB (100781268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a749f5a3a26604fcd3ab38985fb57906669c2c3ca17120d1a73135d7a45894b7`  
		Last Modified: Fri, 14 Mar 2025 19:09:34 GMT  
		Size: 4.3 MB (4305734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd22c9e6bda011162aadd771c38f792aa0187aed5429cc0e633bbe900328301`  
		Last Modified: Fri, 14 Mar 2025 19:09:36 GMT  
		Size: 189.3 MB (189340581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ce7e57041b7c1758daaab6f10de4b4fdabb9e6aa9bfcf66981c10679bc9003`  
		Last Modified: Fri, 14 Mar 2025 19:09:34 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403c9415a26577ea18469178cb467a9bb708026d7f736471e5509ff590b8aba`  
		Last Modified: Fri, 14 Mar 2025 19:09:34 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becb37ff774ad656eb2391799888d3c0e9edfc18a21d8c0374e427b3e66b09e1`  
		Last Modified: Fri, 14 Mar 2025 19:09:34 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ec96aa38d0468ee43483535fd8f688591187cbdb0a1a019dd0d997153d80fb`  
		Last Modified: Fri, 14 Mar 2025 19:09:35 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51732593952e64632d3f4e105877339ba81f9d8c14c5056dd6c58e2a76b81eff`  
		Last Modified: Fri, 14 Mar 2025 19:09:34 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3772db656e5469814bb1d426b846c0707d13fe5b8ccc07f368753aa117f15946`  
		Last Modified: Fri, 14 Mar 2025 19:09:35 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58fc97f7a0c93f794d3123d5ed9d648d1627e51ff9e94917b341ffecbb3a69c`  
		Last Modified: Fri, 14 Mar 2025 19:09:35 GMT  
		Size: 4.8 KB (4832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:f42c97e78927587036f4cf96215487be301bc0654488ef05f3f5586a5de92740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196d533f19ebd60e1df933b72e58957d0cc811d1b4b9afc419c402876ad51827`

```dockerfile
```

-	Layers:
	-	`sha256:bb84c5f3e9792fe3aca8afb7254a44d8e1c59df46eabe6813da89134b721b1c8`  
		Last Modified: Fri, 14 Mar 2025 19:09:34 GMT  
		Size: 32.2 KB (32227 bytes)  
		MIME: application/vnd.in-toto+json
