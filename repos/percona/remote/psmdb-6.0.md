## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:9ac424c4a8111fed162c7d8c006b12d7af992d574c5909934991eb9f90c137d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:b73dad1b8266a63e028a19d67b10a7f35a032022e1cde5ce35d2f5322c33009c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273281720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3b143e96f4a2d4656ee8070cffdcaf2a593176f2ec5b94247777e4fdca1c1c`
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
# Sat, 22 Jul 2023 01:46:26 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 22 Jul 2023 01:46:26 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:46:26 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 22 Jul 2023 01:46:26 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:46:26 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:47:19 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:47:20 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:47:20 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:47:21 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:47:21 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:47:24 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:47:27 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:47:27 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:47:27 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 22 Jul 2023 01:47:28 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:47:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:47:28 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:47:28 GMT
USER 1001
# Sat, 22 Jul 2023 01:47:28 GMT
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
	-	`sha256:204ac45a03315a5f6a8b29c06b73155c99ce39963cc0b373a2204ebf3b39a949`  
		Last Modified: Sat, 22 Jul 2023 01:52:33 GMT  
		Size: 171.5 MB (171466521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bf54010b1edafbe136984c45019fd89c2e4b76e4ade03f7815711bbac9bdbd`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042513575f01729ea24f839a4f1d513648a9d25a33575f1c4908cc97b3889d65`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d9411ec8b7ce61275eb5fe1f03e9d6f749047513cb3aaa771c2abce89d0821`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fb155650ddce25c425d293ced38bfbf03cb3a7b3cfe01162b23e10ffcb3a1b`  
		Last Modified: Sat, 22 Jul 2023 01:52:11 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd16c18633ef245ba79a9db2a6667e94351a8d3db11b3995819f61fe54b149b`  
		Last Modified: Sat, 22 Jul 2023 01:52:12 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bce9efd7e0ed38913c714ed797d5a423ab4aa5358aaee5526e61de9c632e6d0`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0945b528b3fd8c59638a49e6b3b897e3cdf42fc6d914d3a7523921837696d73`  
		Last Modified: Sat, 22 Jul 2023 01:52:10 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
