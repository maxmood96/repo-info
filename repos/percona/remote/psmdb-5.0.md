## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:b8c773c6f0a57a577d393e945b06e781c69cd0efebebc6f6ed5a6e6d4cb19321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:3cd021d565b80f96b8e4dbd0e09984e0e502d6c7071f35f177eefb48d4748412
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210829318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb478e8431ae7cfa45bdc1e06cefb5348bcf0db78d64c15a476470a01196e9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 04 Aug 2022 00:36:24 GMT
ADD file:a5c0188d3e4384a1f788282e3e08114ef4bbdc6c4380027e1bd5bce1bc4e5198 in / 
# Thu, 04 Aug 2022 00:36:25 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 01:27:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Aug 2022 01:29:00 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Thu, 04 Aug 2022 01:29:00 GMT
ENV PSMDB_VERSION=5.0.9-8
# Thu, 04 Aug 2022 01:29:00 GMT
ENV OS_VER=el8
# Thu, 04 Aug 2022 01:29:00 GMT
ENV FULL_PERCONA_VERSION=5.0.9-8.el8
# Thu, 04 Aug 2022 01:29:01 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 04 Aug 2022 01:29:38 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 04 Aug 2022 01:29:40 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 04 Aug 2022 01:29:40 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 04 Aug 2022 01:29:40 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 04 Aug 2022 01:29:40 GMT
ENV GOSU_VERSION=1.11
# Thu, 04 Aug 2022 01:29:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 04 Aug 2022 01:29:46 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 04 Aug 2022 01:29:47 GMT
VOLUME [/data/db]
# Thu, 04 Aug 2022 01:29:47 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 04 Aug 2022 01:29:48 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Thu, 04 Aug 2022 01:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Aug 2022 01:29:48 GMT
EXPOSE 27017
# Thu, 04 Aug 2022 01:29:48 GMT
USER 1001
# Thu, 04 Aug 2022 01:29:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fae47290d1d4680e418ff0e417295a1a662b380f965dde612c1f7602670ffabd`  
		Last Modified: Thu, 04 Aug 2022 00:37:18 GMT  
		Size: 84.6 MB (84583462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6fd6c5ea6c68397c8d6e7a23e1fa217460d11ec939df7f18d9fd89dc67779d`  
		Last Modified: Thu, 04 Aug 2022 01:33:26 GMT  
		Size: 3.7 MB (3747498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fce392acaeb63e555270d5f393f3db97e3b002a956ee988b0bbaa30e5bffe7`  
		Last Modified: Thu, 04 Aug 2022 01:33:39 GMT  
		Size: 113.4 MB (113412309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b30b5b434140f39c4907e110e9c4374db119eea0edc5b1846b19cff5ee5a795`  
		Last Modified: Thu, 04 Aug 2022 01:33:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcf95441a8a111005fe19a4abba60508c98529f35d4727ddf314ff535be704b`  
		Last Modified: Thu, 04 Aug 2022 01:33:24 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa4c43986f10aa3e1bbbbd13de3780fc29411b3ad3e6ddd1ce21ece15fe8320`  
		Last Modified: Thu, 04 Aug 2022 01:33:22 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a464693495f027a23d63336a9d63f99bc7e26540460b1176bb52dcba26ad6a0`  
		Last Modified: Thu, 04 Aug 2022 01:33:23 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c359d31807f7ae1a77593fded57ac34854010e2609ba12f36a197a8abb4b545e`  
		Last Modified: Thu, 04 Aug 2022 01:33:24 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f201d364596c5395ff7bb955c63599a0f2a7afc6abb217e1584c8c8dbfe2a51b`  
		Last Modified: Thu, 04 Aug 2022 01:33:22 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d849d5bd2e80ec998823235ef9760c58e9787a2393af6e5a5e025c6cc77d`  
		Last Modified: Thu, 04 Aug 2022 01:33:22 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
