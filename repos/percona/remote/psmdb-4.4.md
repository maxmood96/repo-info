## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:905433ba9eecbef913684e298070a55cadf6ed31e8b8a0cfd921051dbc653575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:a6798b6652f4fadaec912241aa665939b446f7e2134fc304ce90e15d277370e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195575331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b995013c558cfa596be936e405bd22b595d1016ea6518caf25ee8a19cbe352a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 04 Aug 2022 00:36:24 GMT
ADD file:a5c0188d3e4384a1f788282e3e08114ef4bbdc6c4380027e1bd5bce1bc4e5198 in / 
# Thu, 04 Aug 2022 00:36:25 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 01:27:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Aug 2022 01:29:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Thu, 04 Aug 2022 01:29:58 GMT
ENV PSMDB_VERSION=4.4.15-15
# Thu, 04 Aug 2022 01:29:58 GMT
ENV OS_VER=el8
# Thu, 04 Aug 2022 01:29:58 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Thu, 04 Aug 2022 01:29:58 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 04 Aug 2022 01:30:35 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 04 Aug 2022 01:30:36 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 04 Aug 2022 01:30:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 04 Aug 2022 01:30:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 04 Aug 2022 01:30:37 GMT
ENV GOSU_VERSION=1.11
# Thu, 04 Aug 2022 01:30:40 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 04 Aug 2022 01:30:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 04 Aug 2022 01:30:42 GMT
VOLUME [/data/db]
# Thu, 04 Aug 2022 01:30:43 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 04 Aug 2022 01:30:43 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 04 Aug 2022 01:30:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Aug 2022 01:30:43 GMT
EXPOSE 27017
# Thu, 04 Aug 2022 01:30:43 GMT
USER 1001
# Thu, 04 Aug 2022 01:30:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fae47290d1d4680e418ff0e417295a1a662b380f965dde612c1f7602670ffabd`  
		Last Modified: Thu, 04 Aug 2022 00:37:18 GMT  
		Size: 84.6 MB (84583462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bdfca7b337de152684038ac2f4f984275d45908a2b46d1f8dfdbac882aaf53`  
		Last Modified: Thu, 04 Aug 2022 01:33:52 GMT  
		Size: 3.7 MB (3747466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821a7305de4dadaccbc644ce553df9d310d2d630f3cf5155b12ea3c2bae714f`  
		Last Modified: Thu, 04 Aug 2022 01:34:04 GMT  
		Size: 98.2 MB (98158363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407f1c078af2bd2ada4a5ae957dc6ff8834f7315ebafdcab617cda881aac8acc`  
		Last Modified: Thu, 04 Aug 2022 01:33:51 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c3146618fce69c9a9329e0ed96d476816e4dcd0443678cefc5bb5d2ac6b91e`  
		Last Modified: Thu, 04 Aug 2022 01:33:51 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d507b54300a28ef5fc2a0a4d0c9dde1f4ac785f246391df82daab6b95e1f9c2b`  
		Last Modified: Thu, 04 Aug 2022 01:33:49 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf627fea0e7f67b4947adf53ef0db1fff4007fae25ada6258d932446fc5d08`  
		Last Modified: Thu, 04 Aug 2022 01:33:49 GMT  
		Size: 914.5 KB (914546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ae0d229561ae9cfce4c6c25ec998d3aa9019cace487021d56c1cb676075341`  
		Last Modified: Thu, 04 Aug 2022 01:33:50 GMT  
		Size: 8.1 MB (8137885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c8f4344e919a98ac736ec173940a8d2086b067435456f3729cfd2b4116f535`  
		Last Modified: Thu, 04 Aug 2022 01:33:49 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787bd7189db94dffa58653d16087c6d0181d5fdb1191f2ef31f66a2aa0eecb5c`  
		Last Modified: Thu, 04 Aug 2022 01:33:49 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
