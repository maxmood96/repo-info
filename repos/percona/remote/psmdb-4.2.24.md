## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:f56420e5cb1637937b66aeec6f4bb994a92f6c1e6fda787264025d0ae6b56db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:622e0c5c0660619869931674abfae5c68f0a142a1e4e29d8d5cd4a95aadfa571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231960656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d487ef50e24010e2c38c64389b3abc14813bc46d8acfd4921bd13a7ebfd61b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:16:49 GMT
ENV PSMDB_VERSION=4.2.24-24
# Tue, 16 Apr 2024 20:16:49 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:16:49 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Tue, 16 Apr 2024 20:16:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:16:49 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:16:52 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:17:46 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:17:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:17:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:17:47 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:17:48 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:17:50 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:17:53 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:17:53 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:17:53 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Tue, 16 Apr 2024 20:17:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:17:53 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:17:53 GMT
USER 1001
# Tue, 16 Apr 2024 20:17:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c266668bb7b12d97bb1e32be623f68c14465c80b553d6a292d727cc9ac3d3a5c`  
		Last Modified: Tue, 16 Apr 2024 20:20:59 GMT  
		Size: 4.3 MB (4297902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc6ebaec9c8a51be468a06069bce2502d55d3bc2040062f43126d7791953695`  
		Last Modified: Tue, 16 Apr 2024 20:21:13 GMT  
		Size: 117.8 MB (117774151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759e053ac5e54f4c54d4320515a01a3f19944bbe986810d31d5be066690f11d5`  
		Last Modified: Tue, 16 Apr 2024 20:20:58 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc29878d09537ef56ffe6c6185c5b679d48f4ed1569f5d7b5ab7786a5ce0f3d5`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a6bbe41c784ec26a42c7b0511e7a1bfd70445d361599c61e68ff77e3653ea5`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795aef1b4e64bf3e705358d897b49cb0773a74d319c2deffcaa8d5d9ea32e62`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1954f0407108cf4b93adfd88292ecdafb1b476e76cf8e39044a50672764592e`  
		Last Modified: Tue, 16 Apr 2024 20:20:57 GMT  
		Size: 8.2 MB (8151460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad166018617a7e45fd76058081d4bc368aa94373a8cb7a19d713cf2fcee796`  
		Last Modified: Tue, 16 Apr 2024 20:20:56 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
