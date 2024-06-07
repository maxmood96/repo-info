## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:32c2cd66a3743c33db26125d47c9e343fb2301c8f42d5c9a247217f68fd28e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:f6d421f1e62bcb7b15ff1a4ac044f19756fea5f259b4d9082106a2ec17fed433
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263022990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd54b00f6feaacd88fd7d197c07e51a2e04196a6491d79bf60953155b1810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:59:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 05:01:05 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 07 Jun 2024 05:01:05 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 05:01:05 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 07 Jun 2024 05:01:06 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 05:01:06 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:02:03 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:02:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:02:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:02:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:02:06 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:02:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:02:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:02:12 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:02:12 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 07 Jun 2024 05:02:12 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 07 Jun 2024 05:02:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:02:13 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:02:13 GMT
USER 1001
# Fri, 07 Jun 2024 05:02:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333ae0eecc825cc280e3e2499816ac966ba114caa112b624b56c613c581897`  
		Last Modified: Fri, 07 Jun 2024 05:05:57 GMT  
		Size: 4.3 MB (4311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b859ddc030918c186ce06234efab6b6630c7694c8f1100867179eb20e7a63`  
		Last Modified: Fri, 07 Jun 2024 05:06:44 GMT  
		Size: 148.9 MB (148910273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e15d503e757081627b62b901873ff8882c0da835e7a7c98b88806e4520c296f`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d622a0bbdc622660b5f402106fec3c78eeee9dad098eb92b5d544f4569a3eaf8`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 4.1 KB (4075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b31ac65a1d7a4a5f18e1679c049a4c51a87afc9af8a8a0eb38ae693e8942b0`  
		Last Modified: Fri, 07 Jun 2024 05:06:24 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56c0cb683b71415383cf6d56a210138dd08567939687b3a1cbf2ac3d3286f3`  
		Last Modified: Fri, 07 Jun 2024 05:06:25 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fde1ee5ef5c08d6ea52b7654906334c43084fc7e0a9e11a04f9c66005b69545`  
		Last Modified: Fri, 07 Jun 2024 05:06:26 GMT  
		Size: 8.1 MB (8137901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d064f6bd6355ae0d3af1cd92e5f4eba3bd0234a187a008e81bc2a4fd00d73c`  
		Last Modified: Fri, 07 Jun 2024 05:06:25 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b46104c08228b516c7061b1368156309d85e3c273f6d9c4bb65f1a608f5290`  
		Last Modified: Fri, 07 Jun 2024 05:06:24 GMT  
		Size: 4.6 KB (4556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
