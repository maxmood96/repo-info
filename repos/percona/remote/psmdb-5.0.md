## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:ee5561ecc7ad795406d6ac7a116920fbf6ab61c9dd29dc3e53b05e37ed36fc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:2ec031cd1b4589c3a0287fc0d9d97a6486ffd133fe27006b7036575269a0e828
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263093105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8222ad5d77178c7dbe7fd22aac53086d0bd6dc1fccd111b57acdbd41117af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:41:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:43:10 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 08 Mar 2024 19:43:10 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:43:10 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 08 Mar 2024 19:43:10 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:43:10 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:44:04 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:44:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:44:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:44:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:44:06 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:44:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:44:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:44:11 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:44:12 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Mar 2024 19:44:12 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:44:12 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:44:12 GMT
USER 1001
# Fri, 08 Mar 2024 19:44:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9587e819e22f1da9e25539345bd39f6429f2911cafe6c433bc588563f198089d`  
		Last Modified: Fri, 08 Mar 2024 19:48:47 GMT  
		Size: 4.3 MB (4304196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d9b581cbd02d1ec08e8ac9cf8fc97109d0916cd7065197385a0bf66803f7a5`  
		Last Modified: Fri, 08 Mar 2024 19:49:36 GMT  
		Size: 148.9 MB (148902362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7c204532e44c8f3ab43d178a889534a5c210f0d85510619b86cf277b657abf`  
		Last Modified: Fri, 08 Mar 2024 19:49:18 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bf7efcec6bb93fa2121f9de2fd00b6a7124d7dc2df17cc797b7507442b8ae2`  
		Last Modified: Fri, 08 Mar 2024 19:49:17 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17277d42ba1e087b1cf7c6a03c3c22bdc5bac483b3289b90e45efc54159e7112`  
		Last Modified: Fri, 08 Mar 2024 19:49:16 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b52f897ee0f00f4da3b38fb122b63028e1b42eb6948d0a66a95b9e537cff61`  
		Last Modified: Fri, 08 Mar 2024 19:49:16 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1677cb1b77e96204568415dc760219aa5636bc2e6b07903a930524653b68deed`  
		Last Modified: Fri, 08 Mar 2024 19:49:17 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef777dcb174af13243d2a6818992d5c59dabe5e02b362effbebbfdbd7bedb2`  
		Last Modified: Fri, 08 Mar 2024 19:49:15 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b5624348b624bbb01acd4d60187256e5a904221e953f41e51edeab88c80810`  
		Last Modified: Fri, 08 Mar 2024 19:49:15 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
