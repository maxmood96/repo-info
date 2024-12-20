## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:cc40737a9808ebc2dea3afb14ef06e6326c1fc9e36998fb7a97ca52492d13e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:212483f40376cf40de2632536ad1da071402ccac08db1ba5b70510c3b7e24df0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286535501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41264cea5dbc4e254ab5c448c34cda4855a54eb9ed777952ef520a7946cc7814`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:59:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 07 Jun 2024 04:59:44 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 07 Jun 2024 04:59:44 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:59:44 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 07 Jun 2024 04:59:44 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 07 Jun 2024 04:59:45 GMT
ENV PSMDB_REPO=release
# Fri, 07 Jun 2024 05:00:46 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 07 Jun 2024 05:00:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 07 Jun 2024 05:00:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 07 Jun 2024 05:00:48 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 07 Jun 2024 05:00:48 GMT
ENV GOSU_VERSION=1.11
# Fri, 07 Jun 2024 05:00:52 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 07 Jun 2024 05:00:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 07 Jun 2024 05:00:55 GMT
VOLUME [/data/db]
# Fri, 07 Jun 2024 05:00:56 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 07 Jun 2024 05:00:56 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 07 Jun 2024 05:00:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jun 2024 05:00:56 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 05:00:56 GMT
USER 1001
# Fri, 07 Jun 2024 05:00:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c333ae0eecc825cc280e3e2499816ac966ba114caa112b624b56c613c581897`  
		Last Modified: Fri, 07 Jun 2024 05:05:57 GMT  
		Size: 4.3 MB (4311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9374102091b6de34f2ddfa589353b80ce2b2b880945837b04396d9be376b81f`  
		Last Modified: Fri, 07 Jun 2024 05:06:16 GMT  
		Size: 172.4 MB (172422786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4371d297efd24129c7be6e948344dff64a77e724cc4a66be262ecf219063c973`  
		Last Modified: Fri, 07 Jun 2024 05:05:56 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d326c23dda258451a6d54935a883682971c745c8506363962cbf603bc227d785`  
		Last Modified: Fri, 07 Jun 2024 05:05:56 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138dd2ee986baf9caabd344fcca10e3dbb7b0bdba5fca1a7ad771e7c86830c02`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 10.6 KB (10574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56aa9e0a0a4508d8416e1a4d7aca5984a0b6f7acb4945da297e7ec35b98f27`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa813a9c3fe54bfc09094980b149818db9497eb51ed142df215367ac930dca3d`  
		Last Modified: Fri, 07 Jun 2024 05:05:55 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b84982c5e87b249d4b86fb989fc820edc15186d6b43e98c9c55e0187a4f28e1`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846edf16ad892df4e95b54ed9f29986629d635a2b46e22d1e0e6cc714f9e503c`  
		Last Modified: Fri, 07 Jun 2024 05:05:54 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
