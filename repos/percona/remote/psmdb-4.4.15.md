## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:63fe75a31c979fea214acd395bf747517cbc4c82b71224f5f2f1bfe016ed9247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:23375caeda483c3635846b85d3e7613778ab7ada6df70b02a8f468fe52abc77f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198180355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6733b6a40c1762f0681f6a23bedbd116728e9ddc28edfb968e26411e59416f6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:02 GMT
ADD file:6e8b447e6b9fb44da452809a15105670b9f9699de7b891279644df73840fdbc5 in / 
# Fri, 27 Jan 2023 23:36:03 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:09:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Jan 2023 00:11:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Sat, 28 Jan 2023 00:11:57 GMT
ENV PSMDB_VERSION=4.4.15-15
# Sat, 28 Jan 2023 00:11:57 GMT
ENV OS_VER=el8
# Sat, 28 Jan 2023 00:11:57 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Sat, 28 Jan 2023 00:11:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Jan 2023 00:12:36 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Jan 2023 00:12:38 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Sat, 28 Jan 2023 00:12:38 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Jan 2023 00:12:38 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Jan 2023 00:12:38 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Jan 2023 00:12:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Jan 2023 00:12:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Jan 2023 00:12:45 GMT
VOLUME [/data/db]
# Sat, 28 Jan 2023 00:12:45 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Jan 2023 00:12:45 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 28 Jan 2023 00:12:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Jan 2023 00:12:46 GMT
EXPOSE 27017
# Sat, 28 Jan 2023 00:12:46 GMT
USER 1001
# Sat, 28 Jan 2023 00:12:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:cb5daa5c9242ca98c8c9f4eb3fb173f7c14b869619db2cb0de5316725ee9b63c`  
		Last Modified: Fri, 27 Jan 2023 23:37:36 GMT  
		Size: 88.4 MB (88425154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1483e4539e893ccc33d0d382e536963dda65888b20fad7a5bb99315ee66e34`  
		Last Modified: Sat, 28 Jan 2023 00:15:41 GMT  
		Size: 3.8 MB (3772001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f2273b5657bd8c3193571e00c288578941cd018abfb117c6012dcbf143f8a`  
		Last Modified: Sat, 28 Jan 2023 00:15:52 GMT  
		Size: 96.9 MB (96897148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c3b07ebf0a343ef36b4adcdd3a76e59867a20d5f007aea75c4119a915c3aa1`  
		Last Modified: Sat, 28 Jan 2023 00:15:40 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d05b82685f58ec4832b5c402492300df6e449e5a537d763cf27e316c8d88813`  
		Last Modified: Sat, 28 Jan 2023 00:15:40 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724df343aaf872b1ff5bd3575331e6249087c4b6025de6dbdfe85749b03fa6fd`  
		Last Modified: Sat, 28 Jan 2023 00:15:38 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b8af849081e96879a164966325557cf5288c314e815df8e67bef021763af27`  
		Last Modified: Sat, 28 Jan 2023 00:15:39 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b7e3f866ade2980f99f210ccd574bca294e4268c910a9aed7f241948deb437`  
		Last Modified: Sat, 28 Jan 2023 00:15:40 GMT  
		Size: 8.1 MB (8137897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b8cb31a43784f892bdc536c16e63acccaff5d84cfa0156710953a9a4b63d2c`  
		Last Modified: Sat, 28 Jan 2023 00:15:39 GMT  
		Size: 13.2 KB (13202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d962e89694250039f6d93b058a4d351b464c4831741981b47e526dd5df9141b`  
		Last Modified: Sat, 28 Jan 2023 00:15:38 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
