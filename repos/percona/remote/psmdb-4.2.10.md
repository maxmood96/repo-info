## `percona:psmdb-4.2.10`

```console
$ docker pull percona@sha256:af17aad82d40a565b7d89f2b6b810700b1ace8051bb6613ba6a502cb13573f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.2.10` - linux; amd64

```console
$ docker pull percona@sha256:474022685cc8cf5bc4cde8f7d18f41e7e91e6208103d0ab8e4b72e487c046bc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170345414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d811d4aeecf5879556f450cd36f6baaced7591d5e9e8ee0ec4971c167f1338a`
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
# Tue, 08 Dec 2020 00:50:43 GMT
ENV PSMDB_VERSION=4.2.10-11
# Tue, 08 Dec 2020 00:50:43 GMT
ENV OS_VER=el8
# Tue, 08 Dec 2020 00:50:43 GMT
ENV FULL_PERCONA_VERSION=4.2.10-11.el8
# Tue, 08 Dec 2020 00:50:44 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 08 Dec 2020 00:50:44 GMT
LABEL org.label-schema.schema-version=4.2.10-11
# Tue, 08 Dec 2020 00:50:44 GMT
LABEL org.opencontainers.image.version=4.2.10-11
# Tue, 08 Dec 2020 00:50:51 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Tue, 08 Dec 2020 00:51:21 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 08 Dec 2020 00:51:22 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 08 Dec 2020 00:51:22 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 08 Dec 2020 00:51:23 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 08 Dec 2020 00:51:23 GMT
ENV GOSU_VERSION=1.11
# Tue, 08 Dec 2020 00:51:25 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 08 Dec 2020 00:51:28 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 08 Dec 2020 00:51:28 GMT
COPY file:36bd7798a7bd236f79a692385b6877519fd05ff40f92de87cb1d5c527c35d799 in /entrypoint.sh 
# Tue, 08 Dec 2020 00:51:28 GMT
VOLUME [/data/db]
# Tue, 08 Dec 2020 00:51:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Dec 2020 00:51:28 GMT
EXPOSE 27017
# Tue, 08 Dec 2020 00:51:29 GMT
USER 1001
# Tue, 08 Dec 2020 00:51:29 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5723d1df872fba296abf30e11965659cbfd5fa5e70b089b5f0425a15e6a5683b`  
		Last Modified: Tue, 08 Dec 2020 00:54:48 GMT  
		Size: 19.3 MB (19312686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f62f73716e00e46afb04c206753c5cd5a0a03dc8cd74ac38ae3740c4e00bbb`  
		Last Modified: Tue, 08 Dec 2020 00:54:56 GMT  
		Size: 66.8 MB (66777557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17022f63436b82a959074b329e8415bc67a9e611ade986cf30da8af1d7fe22f3`  
		Last Modified: Tue, 08 Dec 2020 00:54:44 GMT  
		Size: 1.5 KB (1544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bc955135f8961942d529eab9afedf3894d4fc901fe7620cbf9f9dd8c745453`  
		Last Modified: Tue, 08 Dec 2020 00:54:43 GMT  
		Size: 4.1 KB (4075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32a8c7a3b2bbf01d478b8cd5ba29dbd2c22cee8a23e6e0b80e3ce1f8be93ac4`  
		Last Modified: Tue, 08 Dec 2020 00:54:43 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be69a7019d24de6c852b3c4845ece13b8a1d369f382f543a3fe08deb413543bd`  
		Last Modified: Tue, 08 Dec 2020 00:54:44 GMT  
		Size: 914.5 KB (914546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5d0fe2168a89ecdc3973ee96f915256c710134aca0264ac8c8ae2a6c0cc5b1`  
		Last Modified: Tue, 08 Dec 2020 00:54:45 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d071e8dee06e256f01de28f253e73a2ac897f4e6c7bdcb95d694446b1c4d108`  
		Last Modified: Tue, 08 Dec 2020 00:54:43 GMT  
		Size: 4.5 KB (4540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
