## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:082ecf5036913659bd1143a8698fcc426c394e184d8a73d8944f82e950991fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:c2e64144aa3e71c779a2ce42fa17e25f6d89029bd6246630dff01fa383288097
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204fa5281e1c7cefbc78a152995e2699c11be7f966a9dbcc27392f92590fd92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:44:39 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:46:56 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 11 Aug 2023 01:46:56 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:46:56 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 11 Aug 2023 01:46:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:46:57 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:47:45 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:47:46 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:47:46 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:47:46 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:47:46 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:47:50 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:47:52 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:47:52 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:47:52 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:47:52 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 11 Aug 2023 01:47:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:47:52 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:47:53 GMT
USER 1001
# Fri, 11 Aug 2023 01:47:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c45cdbc96586817c8b7bc5b4bd8858798f2d665457878d8f9ba40c3cef93c`  
		Last Modified: Fri, 11 Aug 2023 01:51:12 GMT  
		Size: 3.8 MB (3797128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef92b1ab4af34b9b3cf9ed5057a7a90e47b7d300eccc205c9ec7515e2dec5fb7`  
		Last Modified: Fri, 11 Aug 2023 01:52:28 GMT  
		Size: 135.8 MB (135798666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0314a478ded2fd7a42b9e3ab0495ef3905f8d1837ce28a990947db02d6198522`  
		Last Modified: Fri, 11 Aug 2023 01:52:11 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426f13bb9d4fb516c8ab6490885acacf10072d05b2ccddd23cda042255f5b919`  
		Last Modified: Fri, 11 Aug 2023 01:52:11 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f952409a9d1848b70ded12c6741f7178665afbf2bb255d87ec9e38b189277`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158348ee2cc49aae27a3cdd3baf9260087b5a973479a044e6e7c8d4c85ab9290`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 914.5 KB (914547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d15bc47e848c151e59ae10176b60e4441522a215517b30f875a6b5fab34496`  
		Last Modified: Fri, 11 Aug 2023 01:52:10 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea22b2156f6235633ecd91f31ac7ea06c2a0e7b396a08ff145536bb311c956`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dba217798745766c79c0548c8864ef668d86839137c46678dc7049dd45276f4`  
		Last Modified: Fri, 11 Aug 2023 01:52:09 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
