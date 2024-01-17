## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:dc14ebf9c82ee3efb539c0b30d32ae8b16c3bdfba53e22216136c2459ac22573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:e5daf1e26140cc7ad848d75c16ae13d5a8fc3264c614a5f964953645e4ba799c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263059304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228fca6a3426bf421cb9a37922b93aab9bd650a9981849d610f6e04f2679e64c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:56:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 21:57:59 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 17 Jan 2024 21:57:59 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:57:59 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 17 Jan 2024 21:57:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 21:57:59 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 21:58:55 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 21:58:56 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 21:58:57 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 21:58:57 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 21:58:57 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 21:59:00 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 21:59:03 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 21:59:03 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 21:59:03 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 17 Jan 2024 21:59:03 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 17 Jan 2024 21:59:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 21:59:04 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 21:59:04 GMT
USER 1001
# Wed, 17 Jan 2024 21:59:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5469717c83d3db94c6864191ccdaadcb11e262854368aaac4bce7114ffc496`  
		Last Modified: Wed, 17 Jan 2024 22:03:45 GMT  
		Size: 4.3 MB (4290055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe51feaec667b43ebe4dbfa80ebf39462ae91c8cb762c847c5c64e2648eac89`  
		Last Modified: Wed, 17 Jan 2024 22:04:34 GMT  
		Size: 148.9 MB (148897448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102f581e8d7abb24eac952ccbc4f838541c16fb860289e088a017bd23630b3dc`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030acdccff6cd64780b49f4c9dec9703a09736c19fc281b4c87a61a7ee83fb2`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da24fdeb58cb63596dd3c67daf1a98d79a4ba2c12f59bd25dc108c53283e6a30`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5ab8d3b7cfc45f9c89f455527442657bb537fce12cf24dbb9f65f228679576`  
		Last Modified: Wed, 17 Jan 2024 22:04:15 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c332acb2fb3080151afe9ce0347265aa6a817c8dea9d6a2952e8266e071916c`  
		Last Modified: Wed, 17 Jan 2024 22:04:16 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafa308b191c79311c5cc72ebbcb0afed96ea1cb6efff761e14513eff9aaf27c`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5148a44cc5def52f5cc0a922756c6971799032b9eb5629701026c36423b8ac`  
		Last Modified: Wed, 17 Jan 2024 22:04:14 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
