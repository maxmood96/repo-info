## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:2434bdc36f05dd7e07042c6fa7a720124e44be8258272413e0e1a0af5a51f06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:7ce7e1dd021e1ce821e2609d471975c2ac67ee334fe8eee6db8c0d22996f33bf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250330853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ee8737267229bfb00293e2a379dfe28a1761c48600c808d4f63f3d929e43e0`
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
# Sat, 01 Jun 2024 01:43:19 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 01 Jun 2024 01:43:19 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:43:19 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 01 Jun 2024 01:43:19 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:43:19 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:44:15 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:44:16 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:44:16 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:44:17 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:44:17 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:44:20 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:44:23 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:44:23 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:44:24 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:44:24 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 01 Jun 2024 01:44:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:44:24 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:44:24 GMT
USER 1001
# Sat, 01 Jun 2024 01:44:25 GMT
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
	-	`sha256:849a437aa8e7437bbfe3be1495bc80750d7fdc26fd505c8ce32ceb970f53d109`  
		Last Modified: Sat, 01 Jun 2024 01:49:04 GMT  
		Size: 136.3 MB (136272862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bdb73139948fdb450f407f91bb5e5719fcda6fdcbe81741ae0596b22e1a4d9`  
		Last Modified: Sat, 01 Jun 2024 01:48:47 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e0f5e07de301adaed1e01154d47eaa5c187ff12d66fed797fbbf55d023c61`  
		Last Modified: Sat, 01 Jun 2024 01:48:46 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5382104801e34c28ad905e53274ba42e826eb477001c2c5ab8c387f12b8034`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e51e33d390c47683332802f3f782c82d5d12c53a93338c10a3ef9d9c0275c0a`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 914.5 KB (914548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974510818003ea4918313a2a6fb387f51323e326a84ec342b0efc458f26654df`  
		Last Modified: Sat, 01 Jun 2024 01:48:46 GMT  
		Size: 8.1 MB (8137896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d25102898941994673476a3a0166417076418cc27be3d011b1d8bfd36d3956a`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0de5b89a74693e7c1cafee5c10c44924b090612ed324489c4440456eca54ee8`  
		Last Modified: Sat, 01 Jun 2024 01:48:45 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
