## `percona:psmdb-6.0.19`

```console
$ docker pull percona@sha256:f1d2fabf8e89f45d035dbe9becdc48c19216fc5228a9cf9835f2bcf0a886ffe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.19` - linux; amd64

```console
$ docker pull percona@sha256:973d4a9637ed3461356259f1b64238f21d5846da70eaa30cebcf87e0341846a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295113357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0b8e3b415ca89bb2852608158647a844fa117aff331bc2c9e50901f11606f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Dec 2024 23:50:03 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Dec 2024 23:50:03 GMT
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
	-	`sha256:b2d9645b7a627311307a917af9385030c91e049ec7862656cb4e05f50090c46a`  
		Last Modified: Fri, 06 Dec 2024 01:28:34 GMT  
		Size: 100.8 MB (100777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed10a7c65c3668320bc9569c464e5476aa869e50f6acbbff966495bfd80656`  
		Size: 4.3 MB (4300287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1f525c5952daae690fe97a56ee94521afc7ed3b973fdbb62a4adb79d2375cf`  
		Last Modified: Fri, 20 Dec 2024 21:29:55 GMT  
		Size: 189.1 MB (189083129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fd26565b10f7071e9646ed0c01527f3b2ffb298375cc2c229d34ad8a2cac5`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3aee438dc3e71e8c2094ac74be177f64afd038ee1e563e1e075ec937d888c8`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73e4fec943efb2f88f46ac0028d2e8f8b0c3b0b8bae5cf3a009fe9b74a9b64`  
		Last Modified: Fri, 20 Dec 2024 21:29:51 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdb862443642d7f877c8aac2cf91b2edd59fd6ce92cf4b0987befb6f1213bee`  
		Last Modified: Fri, 20 Dec 2024 21:29:54 GMT  
		Size: 914.5 KB (914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d25e61c119f3fa3c7aa25285de408851d34d20013cced88b80b69def9fa924`  
		Last Modified: Fri, 20 Dec 2024 21:29:54 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f9aaa8b44ef52a2c51e6822dbf1a238ed11685e6bce31a078a0c4d52d19dd2`  
		Last Modified: Fri, 20 Dec 2024 21:29:54 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5162dfce43b766555829c1240bf47376045efd134569ec9e8b2fdb347a6824`  
		Last Modified: Fri, 20 Dec 2024 21:29:55 GMT  
		Size: 4.8 KB (4834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.19` - unknown; unknown

```console
$ docker pull percona@sha256:cd8b8a042d8c1751b40ac0729ba18458c9c32942316ba63c9dc1d2fab480b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c499eabbf4d29115e4bf9c683fadb62e765ea7cc95c83c8f35e88d5e09635`

```dockerfile
```

-	Layers:
	-	`sha256:12c7973b554c20191044f6681aabd61fb430fbe6854418d59f714adefc6a67c7`  
		Last Modified: Fri, 20 Dec 2024 21:29:53 GMT  
		Size: 32.2 KB (32227 bytes)  
		MIME: application/vnd.in-toto+json
