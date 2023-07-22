## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:ce9b4da67e41a942df161bfdea39727f996063a307ddde59129a1a91167be2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:b7916dd2b6e8464b9a18e349dbe9d904cebd6bac4c17f14b8562e53b46fab4cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237613434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b78758d1c0bb970d51df4954d754e2f3c683b22665fc89cb8be5d0c80d44ec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:46:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:48:43 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 22 Jul 2023 01:48:43 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:48:43 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 22 Jul 2023 01:48:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:48:43 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:49:32 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:49:34 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:49:34 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:49:34 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:49:34 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:49:37 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:49:39 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:49:39 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:49:40 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:49:40 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 22 Jul 2023 01:49:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:49:40 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:49:40 GMT
USER 1001
# Sat, 22 Jul 2023 01:49:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6085e88023bbde8302c7985668868ba6553a08d034735742781e00526443c8`  
		Last Modified: Sat, 22 Jul 2023 01:52:14 GMT  
		Size: 3.8 MB (3801618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc79af77c7d33948209cb4ab3b7c748b48915e5e82605f46fdd97a7e7c1df3`  
		Last Modified: Sat, 22 Jul 2023 01:53:32 GMT  
		Size: 135.8 MB (135798244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a507dba314d7c69087bf0b3ee2474ffef7e5499b6cf2a5a235363b154bac26`  
		Last Modified: Sat, 22 Jul 2023 01:53:15 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8e2ebfbee8e0b99ef6552f2ba3bc1a49b1d0f74574b3017e7cbf18b377307a`  
		Last Modified: Sat, 22 Jul 2023 01:53:15 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95390feb4e5ca96441e52c5692d764a473ca4c36264a9bfdd4a5a43695396c9`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ada12120e29efb25592448d1a953981c58c7e8bd80e12b8555076400848084`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf52c6c31b49cf96cd4e9c052d07320fb813d4f1823dc905c403838263347c4b`  
		Last Modified: Sat, 22 Jul 2023 01:53:14 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68627a4717e1892f28e31967dd09568e9857744cb956c2e96717190acb0581ae`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a58f08dfffc0689e3c9e4f91b911f776957437bdc4d2199a0d80deb29059ece`  
		Last Modified: Sat, 22 Jul 2023 01:53:13 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
