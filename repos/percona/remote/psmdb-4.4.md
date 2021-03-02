## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:fbf661e4efe72c2090c26e2650384bee24ccb9440da55ccf378ee52ad7315daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:a4e832a33d728b1fa7be35a34a133a05a7fc8bdd25e80ebc0ce5dea1daf54e58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200373422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89b59cb0fa4748d8c95f090b87906c7aea16a8bbff3f44dc87e717a67879622`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:48:03 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 21 Dec 2020 20:52:15 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Tue, 02 Mar 2021 00:27:52 GMT
ENV PSMDB_VERSION=4.4.4-6
# Tue, 02 Mar 2021 00:27:52 GMT
ENV OS_VER=el8
# Tue, 02 Mar 2021 00:27:52 GMT
ENV FULL_PERCONA_VERSION=4.4.4-6.el8
# Tue, 02 Mar 2021 00:27:53 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 02 Mar 2021 00:28:22 GMT
RUN set -ex;     dnf install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         oniguruma         jq         dnf-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     dnf clean all;     dnf -y remove dnf-utils;     rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 02 Mar 2021 00:28:24 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 02 Mar 2021 00:28:24 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 02 Mar 2021 00:28:25 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 02 Mar 2021 00:28:25 GMT
ENV GOSU_VERSION=1.11
# Tue, 02 Mar 2021 00:28:27 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 02 Mar 2021 00:28:30 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 02 Mar 2021 00:28:30 GMT
COPY file:1e164890dbc426ff0038117af76a47815ae534b64e95a15a83e6e5d7f79a4d77 in /entrypoint.sh 
# Tue, 02 Mar 2021 00:28:30 GMT
VOLUME [/data/db]
# Tue, 02 Mar 2021 00:28:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Mar 2021 00:28:30 GMT
EXPOSE 27017
# Tue, 02 Mar 2021 00:28:30 GMT
USER 1001
# Tue, 02 Mar 2021 00:28:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2acf9799d0998bd2c0650b3450cdfa5c5a4dd09a53a5d2107305b0e99b208b8`  
		Last Modified: Mon, 21 Dec 2020 20:58:18 GMT  
		Size: 19.5 MB (19481136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b521d9124cc5e793dc476ce6d615edee507fc557f3d8a0e8d8195d47791d14`  
		Last Modified: Tue, 02 Mar 2021 00:29:44 GMT  
		Size: 96.6 MB (96637112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437795d874f95a4cd5422be7f64d8a176f5a0bd3d07477514b3e849c44409789`  
		Last Modified: Tue, 02 Mar 2021 00:29:30 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1571891d627205eb58c64424085ec08fa0a67e09e3e40d8f486cfdbd4d8d2bd8`  
		Last Modified: Tue, 02 Mar 2021 00:29:28 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9ef4e0875508eed0b7c08ae3b8750aa3acd847da02a393782a14994cac10d4`  
		Last Modified: Tue, 02 Mar 2021 00:29:28 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20d3c97c98d4ab4a01d049f8080162a2bf6df692a0669db221ccdfc5829f3e4`  
		Last Modified: Tue, 02 Mar 2021 00:29:28 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5614b10990e80439836a96f17a96f1e4b0ff69754fb64b9a1e7174e596e66b`  
		Last Modified: Tue, 02 Mar 2021 00:29:30 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc675085a51e6be464d8419739b8523ff968df62967e0eea94b6678623bbe99`  
		Last Modified: Tue, 02 Mar 2021 00:29:28 GMT  
		Size: 4.5 KB (4544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
