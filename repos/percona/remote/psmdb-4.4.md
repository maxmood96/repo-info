## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:5b8a01325eaf7b1554e8d56767fc4928e9a6390826746116d85c262a10b50c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:9802cb8b6fd763b91b905cb08172d9cd3df538cdd6d864519792ce1ffd3f2be3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250478954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38911558e4a7c525072fee3a730ca16ece26e8150d38cb65c29b893a1654068a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:13:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:15:39 GMT
ENV PSMDB_VERSION=4.4.22-21
# Tue, 16 Apr 2024 20:15:39 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:15:39 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Tue, 16 Apr 2024 20:15:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:15:39 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:16:35 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:16:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:16:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:16:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:16:37 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:16:40 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:16:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:16:42 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:16:43 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 16 Apr 2024 20:16:43 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Tue, 16 Apr 2024 20:16:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:16:43 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:16:43 GMT
USER 1001
# Tue, 16 Apr 2024 20:16:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a5e0a2bb3cc381a5bdd2bea8cea5f6d155fa0c806c57d7ba868968cab01fc2`  
		Last Modified: Tue, 16 Apr 2024 20:19:12 GMT  
		Size: 4.3 MB (4297849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e6b154e5c9a7239842022b618c96b2eb9c3d4e336c5e5c7ce570520c00d481`  
		Last Modified: Tue, 16 Apr 2024 20:20:46 GMT  
		Size: 136.3 MB (136292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f2a17fd8a1031cf0cafeafdd51d756ef351523e86cd29346574838830e18e0`  
		Last Modified: Tue, 16 Apr 2024 20:20:29 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ff7d255661a520d7d1980d71a5e983a28dd790bc6f1984fdc504c7818b0966`  
		Last Modified: Tue, 16 Apr 2024 20:20:29 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a960df54a5e0b7ebb0e8bea1a8e5bec0a33e66e553a86bedcfadda721206ec`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b176072f3e9badf0c33f65fa2b6ea846b92099783bb6a1409e5d8c1d835d39cd`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 914.5 KB (914541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473ef27e48b3024c48119cd6369ef32f5b495ca7dad625d080ec50bc17ec8737`  
		Last Modified: Tue, 16 Apr 2024 20:20:28 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3e3b3df285ae10dade831714414f3d34a3cb7f2a9ad4f233dd7462264dbe5`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c05b7bd9870df5026cf9cb0d5044d5f39368c2e142ffb8378fd05cf8d1a1f95`  
		Last Modified: Tue, 16 Apr 2024 20:20:27 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
