## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:382b30d8c925811eb4f77f9d504705d4d9af72983922a2d9ccd7bc2ea0eb1624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:aa7e54a4b7e946ea50dc44cdbca34339572de5161556fdb841fd231204b19e6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250223819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f6b60f22d3c352c4bd3e7550f43bf07301e07c16e8b2312ada7a1062d6e715`
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
# Sat, 22 Jul 2023 01:47:33 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 22 Jul 2023 01:47:33 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:47:33 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 22 Jul 2023 01:47:33 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:47:33 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:48:23 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:48:24 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:48:24 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:48:25 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:48:25 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:48:27 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:48:30 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:48:30 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:48:31 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:48:31 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:48:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:48:31 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:48:31 GMT
USER 1001
# Sat, 22 Jul 2023 01:48:31 GMT
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
	-	`sha256:6530c77d4061f301dc34466e1923c214a777e1bc493cc2425b2cc9155989b359`  
		Last Modified: Sat, 22 Jul 2023 01:53:02 GMT  
		Size: 148.4 MB (148408642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0785a0c71196b769fa2ba8f8c9751cf1db7396456fe22fe7b9980a8b765f6ba`  
		Last Modified: Sat, 22 Jul 2023 01:52:44 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3921a48dd375b61e19241e9792d095a5595ac9a4a141161211b8158fc9f86fe1`  
		Last Modified: Sat, 22 Jul 2023 01:52:44 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9943d42580bf59253114c86cf504850073eb84721926aa1f58fd200937f4409a`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ca833f799b9eb4728b8c7698afe74920c15d0078a8c7021b24d2f321b1afd0`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bfe35eef2a5b5649572e5da484c166e974ead34bdfb83c065677b636b5525b`  
		Last Modified: Sat, 22 Jul 2023 01:52:43 GMT  
		Size: 8.1 MB (8137883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c8da5f61229ba5b954d14e7dae0ac5008feb2639800e1bbf1198298cb638e8`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99922085625f2fb09526d7e5905cdff8c77138b9f50db9136a2c809e4d03f9`  
		Last Modified: Sat, 22 Jul 2023 01:52:42 GMT  
		Size: 4.6 KB (4560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
