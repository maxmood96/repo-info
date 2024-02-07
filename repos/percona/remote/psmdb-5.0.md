## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:30b578806680d30ab04027072e5e794ceb263ecbca030052072d2141018eab4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:23c97954fa38dff5cbf667e067052b91182021f361bba4f40cf800cdc0a130d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263051645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b143dd56e1794267ad2c10a74cf4c2f67b77a637fdc27cf9a6cd5d4ce158bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:44:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:45:39 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 07 Feb 2024 06:45:39 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:45:39 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 07 Feb 2024 06:45:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:45:39 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:46:33 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:46:34 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:46:34 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:46:35 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:46:35 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:46:38 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:46:40 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:46:40 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:46:41 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 07 Feb 2024 06:46:41 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 07 Feb 2024 06:46:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:46:41 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:46:41 GMT
USER 1001
# Wed, 07 Feb 2024 06:46:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314119ed78ebc3b5e2d56ca8949da4b1484d32443c778cfdee52e1e0b414ae45`  
		Last Modified: Wed, 07 Feb 2024 06:51:16 GMT  
		Size: 4.3 MB (4284810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70886cf0afd4f86e6071e89c3c757e1713fcf3a396fc2d8b0aab67630f962487`  
		Last Modified: Wed, 07 Feb 2024 06:52:09 GMT  
		Size: 148.9 MB (148897065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9cd589b2134e60f19a1c3eba1a338e82424a1eaf318a79cbe422dbd7834b9e`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7041e03e34ddb7d3cda94fdf1ec2f6c2a9364e5cf64d73839d36aa370f54cfd9`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f730048d553e8b5a9213999f5c9a054ceb3dcebf4422ad8f009b61e319bcfa91`  
		Last Modified: Wed, 07 Feb 2024 06:51:46 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a485b5dad5105b62b4926b368fed74a00fa67e3ed9c35d41e12eb69875d25`  
		Last Modified: Wed, 07 Feb 2024 06:51:47 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c297790844148ad2dc1b5a68d02330db5afadeadf53b3cfaea5dfa16b15a5d5b`  
		Last Modified: Wed, 07 Feb 2024 06:51:48 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a14df46e5359e9eabd6d654e59cb97eebea774edff6e9a5c7e0984a7eea53`  
		Last Modified: Wed, 07 Feb 2024 06:51:46 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97e96658e3b92b21e60cf796061da2797c2f65791bf5e9581f11755ad36e624`  
		Last Modified: Wed, 07 Feb 2024 06:51:47 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
