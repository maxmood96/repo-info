## `percona:psmdb-4.4.1`

```console
$ docker pull percona@sha256:c405e40f772fe432b9fc07abeb634b68b7b80bc98cf984314034d3e8607535d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.4.1` - linux; amd64

```console
$ docker pull percona@sha256:a82f9094ac4313316b2d9e3f5dc2473d864ef3db985c4f141eaf7b062362135e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181833228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213549748cf2b211d91755fb829bdd2d76bb2a27a2045f7734edd47335bccc3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:49:57 GMT
LABEL org.label-schema.schema-version=1.0
# Tue, 08 Dec 2020 00:49:57 GMT
LABEL org.label-schema.name=Percona Server for MongoDB
# Tue, 08 Dec 2020 00:49:57 GMT
LABEL org.label-schema.vendor=Percona
# Tue, 08 Dec 2020 00:49:57 GMT
LABEL org.label-schema.description=Percona Server for MongoDB is our free and open-source drop-in replacement for MongoDB Community Edition. It offers all the features and benefits of MongoDB Community Edition, plus additional enterprise-grade functionality.
# Tue, 08 Dec 2020 00:49:57 GMT
LABEL org.label-schema.license=SSPLv1
# Tue, 08 Dec 2020 00:49:57 GMT
LABEL org.opencontainers.image.title=Percona Server for MongoDB
# Tue, 08 Dec 2020 00:49:58 GMT
LABEL org.opencontainers.image.vendor=Percona
# Tue, 08 Dec 2020 00:49:58 GMT
LABEL org.opencontainers.image.description=Percona Server for MongoDB is our free and open-source drop-in replacement for MongoDB Community Edition. It offers all the features and benefits of MongoDB Community Edition, plus additional enterprise-grade functionality.
# Tue, 08 Dec 2020 00:49:58 GMT
LABEL org.opencontainers.image.license=SSPLv1
# Tue, 08 Dec 2020 00:49:58 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 08 Dec 2020 00:49:58 GMT
ENV PSMDB_VERSION=4.4.1-3
# Tue, 08 Dec 2020 00:49:59 GMT
ENV OS_VER=el8
# Tue, 08 Dec 2020 00:49:59 GMT
ENV FULL_PERCONA_VERSION=4.4.1-3.el8
# Tue, 08 Dec 2020 00:49:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 08 Dec 2020 00:49:59 GMT
LABEL org.label-schema.schema-version=4.4.1-3
# Tue, 08 Dec 2020 00:49:59 GMT
LABEL org.opencontainers.image.version=4.4.1-3
# Tue, 08 Dec 2020 00:50:10 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Tue, 08 Dec 2020 00:50:29 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 08 Dec 2020 00:50:30 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 08 Dec 2020 00:50:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 08 Dec 2020 00:50:31 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 08 Dec 2020 00:50:31 GMT
ENV GOSU_VERSION=1.11
# Tue, 08 Dec 2020 00:50:34 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 08 Dec 2020 00:50:36 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 08 Dec 2020 00:50:36 GMT
COPY file:1e164890dbc426ff0038117af76a47815ae534b64e95a15a83e6e5d7f79a4d77 in /entrypoint.sh 
# Tue, 08 Dec 2020 00:50:36 GMT
VOLUME [/data/db]
# Tue, 08 Dec 2020 00:50:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Dec 2020 00:50:37 GMT
EXPOSE 27017
# Tue, 08 Dec 2020 00:50:37 GMT
USER 1001
# Tue, 08 Dec 2020 00:50:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d626aa99fae5a6d007be9acdd14fec57b0cf8cc02cb7feaedab9a1fd45f40b`  
		Last Modified: Tue, 08 Dec 2020 00:54:31 GMT  
		Size: 19.3 MB (19312630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389bd89b605e2a1ec72f4eeb864e971413cad83ba9d6225da304b1efdbbabb6b`  
		Last Modified: Tue, 08 Dec 2020 00:54:37 GMT  
		Size: 78.3 MB (78265419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc76837ef87dc4247bf2a2e9d1d474bcdaaf97fb6e79f27417a9a390de0b0e3`  
		Last Modified: Tue, 08 Dec 2020 00:54:25 GMT  
		Size: 1.5 KB (1543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc30d91a61866ca448d60682c2353dee760cd4ca0419bfcd9eba00b94407119d`  
		Last Modified: Tue, 08 Dec 2020 00:54:23 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe008bf9496a5b462774354c3dd4c99b8fed5e1c675ef667823e4c0a1382149e`  
		Last Modified: Tue, 08 Dec 2020 00:54:24 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d977079d3aa2594d193acf398b38b61155c278f449490134dc8438de06c0d7`  
		Last Modified: Tue, 08 Dec 2020 00:54:23 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904262524fbb419c032ad192d972fb3535b89b51cecf5e5e50c39aa0fe7237cf`  
		Last Modified: Tue, 08 Dec 2020 00:54:26 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5953048d1690331934521c94e24711187734c85e8dcff0d5e28e8dd11684c7`  
		Last Modified: Tue, 08 Dec 2020 00:54:24 GMT  
		Size: 4.5 KB (4545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
