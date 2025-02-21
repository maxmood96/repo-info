## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:265b3fcad37b643a26216d8e309a94f1756d27223788569f917da8c6f32ac3f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:643a60893fbb6bafb095ee9628b8d363525c816aead2ca162c5509220304cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295416328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c136fa4ea46d58bdf16d49757daf44ae93ad3b015834a9cd1cc867964fdfa202`
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
	-	`sha256:148ed553d11fdee385e8b66150a974b767ce6f15a19eaa19fed8de02e10dc0e9`  
		Last Modified: Thu, 20 Feb 2025 02:28:16 GMT  
		Size: 100.8 MB (100789798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67725bb83a61ab3e83637661475b294ed97c2f5e70e4e8750e4cb596001ce17`  
		Last Modified: Thu, 20 Feb 2025 04:11:54 GMT  
		Size: 4.3 MB (4318205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b259e4de95cb4389e1c13a3fd60711adc59133a018c5482554064460b949fb`  
		Last Modified: Thu, 20 Feb 2025 04:11:57 GMT  
		Size: 189.4 MB (189355933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3448248d6cb87e8ce91063f329789c70c01cc193404815777cf402abda920be8`  
		Last Modified: Thu, 20 Feb 2025 04:11:54 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c9d9c94e8f13087dc6ebcbe83d2df9d2bfcabc7fd89b7139a05d3f1437fb52`  
		Last Modified: Thu, 20 Feb 2025 04:11:54 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f3be50a021dad962a96b853855fa1e8250eb402ce078468f7f2351e1421e24`  
		Last Modified: Thu, 20 Feb 2025 04:11:55 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61410f7e6ed7e4e2fdba3da3e05551c68458622f1884d5d83fd5773fdc9afbec`  
		Last Modified: Thu, 20 Feb 2025 04:11:55 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b06e2d70b56afa1ef5b2f1ecc0b53de672f0e0f75cfed0ce83197a9b94bffc4`  
		Last Modified: Thu, 20 Feb 2025 04:11:55 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6400a95bfed29fae38bfd0dfeee4e7c327076cad2564a3e49d34d2c990ac635`  
		Last Modified: Thu, 20 Feb 2025 04:11:55 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab80fefb8259f4681f9e84611d24ae4d3b9584e13ebe146e01c1168eaac71f1`  
		Last Modified: Thu, 20 Feb 2025 04:11:56 GMT  
		Size: 4.8 KB (4832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:e147caefea8d1b38507b33ef31a530495c7964339ba1afeb78fbda9acfd468e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adcf78e8831b95a785e86d31503d1e98512e5a20bd887444ad64403a385feea`

```dockerfile
```

-	Layers:
	-	`sha256:77984d3e073e822ec59b8f0a57988b7fd0a1e2ac75258d6c6b8d25c57615a782`  
		Last Modified: Thu, 20 Feb 2025 04:11:54 GMT  
		Size: 32.2 KB (32226 bytes)  
		MIME: application/vnd.in-toto+json
