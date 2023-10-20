## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:c4c9ec2e4d3afad1979cd2f1456ba3cb3391f709a342945e056289acba7bbd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:5cef7dfd8e38103ce134545850f1d69e77c47c8da95edda57525de5b26515e0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249303274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de03226b2b13f63764d376aedf876266afec4dd545967e9173d3ca7f8c9b156`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:51:15 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 20 Oct 2023 18:51:15 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:51:15 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 20 Oct 2023 18:51:15 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:51:15 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:52:07 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:52:08 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:52:08 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:52:08 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:52:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:52:11 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:52:13 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:52:13 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:52:14 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 20 Oct 2023 18:52:14 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:52:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:52:14 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:52:14 GMT
USER 1001
# Fri, 20 Oct 2023 18:52:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0fe297be2aecc89679b1cd2a34b3e156a5ceb5647404173faeee333a0d2f8`  
		Last Modified: Fri, 20 Oct 2023 18:57:03 GMT  
		Size: 3.8 MB (3797309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6c785ca3a6fc517f1ba95a76c07abafa8684d465949dd4a1ababdaccae046`  
		Last Modified: Fri, 20 Oct 2023 18:57:51 GMT  
		Size: 148.4 MB (148415890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ed5695fb2672d04a5850c0aea73ea95914a13ff36b7e9a9bedcf8670bd6e1`  
		Last Modified: Fri, 20 Oct 2023 18:57:34 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ed65b64b1416138d3570a58560feb319a70fc6eb47e75a7b3db6a3cd8e4165`  
		Last Modified: Fri, 20 Oct 2023 18:57:34 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214e38aea4a7fcf729fe79b1ae1c8b8a4099cf172dc4ae781f7ef0c9236267f4`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9be724c7b226f4fd713f609122402617f49aa061abe71ec550bcfa7f003bf2c`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbad2e3b812c4ef4531a43fb396a68b3033af65beb7c207424e2c8b18326dd06`  
		Last Modified: Fri, 20 Oct 2023 18:57:33 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66459148337569d2008b5bc277f313d2f2f27199f74b0b2ef0c4eb7d4150415`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7b049ff67cf7d690c2893e1f4a928baa052006e8f3bb55f990d9b994767fd5`  
		Last Modified: Fri, 20 Oct 2023 18:57:32 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
