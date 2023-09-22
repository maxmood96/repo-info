## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:80faad07173c012639ad488cc39a898c46d475471628230cdba6734676f6544a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:45e90b9b33ede988dda0545791eaf540ccaf578bf90bfa571ec575fae87015d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250248787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc412e71421c75f0eb54b188104d5de541b9f6f7ab5a4a5df1940cc620d47b65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 21 Sep 2023 23:23:50 GMT
ADD file:f1400f7c015d009a734ef72b857aca20fa0b646827d6d6c0fbd1ec44314f40f1 in / 
# Thu, 21 Sep 2023 23:23:51 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:45:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 21 Sep 2023 23:47:21 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 21 Sep 2023 23:48:28 GMT
ENV PSMDB_VERSION=5.0.18-15
# Thu, 21 Sep 2023 23:48:28 GMT
ENV OS_VER=el8
# Thu, 21 Sep 2023 23:48:28 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Thu, 21 Sep 2023 23:48:28 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 21 Sep 2023 23:48:29 GMT
ENV PSMDB_REPO=release
# Thu, 21 Sep 2023 23:49:20 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 21 Sep 2023 23:49:21 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 21 Sep 2023 23:49:21 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 21 Sep 2023 23:49:22 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 21 Sep 2023 23:49:22 GMT
ENV GOSU_VERSION=1.11
# Thu, 21 Sep 2023 23:49:25 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 21 Sep 2023 23:49:27 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 21 Sep 2023 23:49:27 GMT
VOLUME [/data/db]
# Thu, 21 Sep 2023 23:49:28 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 21 Sep 2023 23:49:28 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Thu, 21 Sep 2023 23:49:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Sep 2023 23:49:28 GMT
EXPOSE 27017
# Thu, 21 Sep 2023 23:49:28 GMT
USER 1001
# Thu, 21 Sep 2023 23:49:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f757f4fc3d201c5d7b9b19e3dbf0ddd78af45972be1834845cecc8fe6a2a5c27`  
		Last Modified: Thu, 21 Sep 2023 23:25:04 GMT  
		Size: 89.0 MB (88977617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4003a78974f8ca57a809c807ac3f02353b39f1aa83d1277ed078d6aa349848`  
		Last Modified: Thu, 21 Sep 2023 23:53:09 GMT  
		Size: 3.8 MB (3793031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71463b6949c581a6489b97e1680e0743bb91e96a019d1f684fc9592691aa91f4`  
		Last Modified: Thu, 21 Sep 2023 23:53:59 GMT  
		Size: 148.4 MB (148391578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af179e9cadd6f75d656a8f600e75d1b6c0ac1fad33b58ca2e146e2ffea58be0`  
		Last Modified: Thu, 21 Sep 2023 23:53:40 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a34a8d4cf13f577f7604c95316720fd79ba0cac1370f92f353876ad971fd23`  
		Last Modified: Thu, 21 Sep 2023 23:53:40 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07395f870b73b1e38dccb5b747c679aeadc369ff2f13682f2bc3b460616cb5`  
		Last Modified: Thu, 21 Sep 2023 23:53:39 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132af750d0b57cc1a5b8eea9e1c1166934b402582732603d9663bcd6a7844804`  
		Last Modified: Thu, 21 Sep 2023 23:53:39 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bd77209473907a86e1dc98bb2aff7aa697a59a780528c306c8f08cbe1df3dc`  
		Last Modified: Thu, 21 Sep 2023 23:53:40 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a463d116ab9c12cdbd4f0fd45203f155e4d8a0e413df54d0e655a8a282df4c03`  
		Last Modified: Thu, 21 Sep 2023 23:53:39 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bbe05006ea5e8c363a56378a9a253110c210475f7bd091239db7b23c21e0f1`  
		Last Modified: Thu, 21 Sep 2023 23:53:39 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
