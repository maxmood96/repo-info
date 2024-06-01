## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:48f78ebf742a35ea55376c3cca396780c28bbacfd2ee1357f69359f08edadce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:df1a54b6cee49216889445b884a4d14d3a9a6b99b99e0d5b7b25e3d75a06cc45
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286455682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42522f485271f9748885c56323b6bc803feab43fef8e286bdbe0bbe6eacae6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:40:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:40:34 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 01 Jun 2024 01:40:34 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:40:34 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 01 Jun 2024 01:40:34 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:40:34 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:41:35 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:41:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:41:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:41:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:41:37 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:41:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:41:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:41:44 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:41:45 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:41:45 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:41:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:41:45 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:41:45 GMT
USER 1001
# Sat, 01 Jun 2024 01:41:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3bd182f766d84adb9d6a9fb3354c19a49292e916414fba6542e8dcf0e2a5b`  
		Last Modified: Sat, 01 Jun 2024 01:47:46 GMT  
		Size: 4.3 MB (4284324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52eeebf7e9015b99a65edf866b86682b1d745a0050eeb7a476d6a24b9090f4c8`  
		Last Modified: Sat, 01 Jun 2024 01:48:06 GMT  
		Size: 172.4 MB (172397673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0c1ecc7a4744158d8a26c9107ddd591df11677a7f064f85cbd372897c85d39`  
		Last Modified: Sat, 01 Jun 2024 01:47:45 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259af95ff3d778451f2bfcb7bfcb6d62236cbaedc4b0d6413b1cac0741f0df1a`  
		Last Modified: Sat, 01 Jun 2024 01:47:44 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e12b7e434a5d9eac09b03796cd6c5a8694329002efae544432a501922ef94e3`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f514f8ad82fc8266547a06e30aa7642ca6e66e06109f7b35dfdd65ac7f9646`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912e7ca9d0ddb57b2d4cbd3ab4f4b52c501e72fe990b07574df2d721f0bf5fc`  
		Last Modified: Sat, 01 Jun 2024 01:47:44 GMT  
		Size: 8.1 MB (8137901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d966888f337f1f37a7c35d9703c8de57eeff6b56ab33bf2a2b458e614173b1ed`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7235e535bf5e070e7a5b7b9c630d3295196113422bb801a1ba1dd973b368a1`  
		Last Modified: Sat, 01 Jun 2024 01:47:43 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
