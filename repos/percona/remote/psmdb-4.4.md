## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:dcbc90378fee63fbdc4d917e7c5bc05815f3dd501e25c1e69f6a83cdb5642fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:4c768650804d30b4f09f1d24b34350f377fca2ab119210a01d578591dbc79f73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194561521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188fd45e2463068d9ab0905764bffd054652488066526e6f88713ab378da899f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:07 GMT
ADD file:9a374ea666c7366668418b8af9d065177ddb8d6d06c691efd448c1782a7202bf in / 
# Wed, 24 Aug 2022 19:35:08 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 22:54:19 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 24 Aug 2022 22:56:48 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 24 Aug 2022 22:56:48 GMT
ENV PSMDB_VERSION=4.4.15-15
# Wed, 24 Aug 2022 22:56:48 GMT
ENV OS_VER=el8
# Wed, 24 Aug 2022 22:56:48 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Wed, 24 Aug 2022 22:56:48 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 24 Aug 2022 22:57:24 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 24 Aug 2022 22:57:25 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 24 Aug 2022 22:57:25 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 24 Aug 2022 22:57:26 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 24 Aug 2022 22:57:26 GMT
ENV GOSU_VERSION=1.11
# Wed, 24 Aug 2022 22:57:28 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 24 Aug 2022 22:57:30 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 24 Aug 2022 22:57:30 GMT
VOLUME [/data/db]
# Wed, 24 Aug 2022 22:57:31 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 24 Aug 2022 22:57:31 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 24 Aug 2022 22:57:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Aug 2022 22:57:31 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:57:31 GMT
USER 1001
# Wed, 24 Aug 2022 22:57:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:aaa7eee1c5ce4029df4c0919904d64a8ee908a0d06ce6618fcb69158082582bf`  
		Last Modified: Wed, 24 Aug 2022 19:36:47 GMT  
		Size: 84.9 MB (84857067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fe316cc797478fc4978cf14f950b71f09cd98d8bfaefea376be4dc9373b403`  
		Last Modified: Wed, 24 Aug 2022 23:00:33 GMT  
		Size: 3.7 MB (3744776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c028c5f8bcd58bf8cf4a7c604c60b7852411ac037d1554c634759ebd1755763`  
		Last Modified: Wed, 24 Aug 2022 23:00:44 GMT  
		Size: 96.9 MB (96873634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036520e8b299ba1a262b8926af2a184d8b38e6f6b7c9b4d6b749bb254fdc0046`  
		Last Modified: Wed, 24 Aug 2022 23:00:32 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcf0c57628445ecc6abc3e5f27fc091c5224ae9d2a72db1b1ee843e0a81abc4`  
		Last Modified: Wed, 24 Aug 2022 23:00:32 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a69def48a183f43b0cd0fbafcafa87622b860215db79147f61ded177e3e6e1`  
		Last Modified: Wed, 24 Aug 2022 23:00:29 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae40d12ec21b2a134771a40607c9e54b3ba8d41c5860c9b965d88e7640a3016`  
		Last Modified: Wed, 24 Aug 2022 23:00:30 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98c5ef8a2afc54bc4a6163795f6a561516fcf6e747249aa445ebbda300c719d`  
		Last Modified: Wed, 24 Aug 2022 23:00:31 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d57b989eb66a082a3649db573bd7282cfce4ec863aed27fd04ad84aaec874`  
		Last Modified: Wed, 24 Aug 2022 23:00:30 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f982edfd1ec38c4cf30984e3b996072c9177b2ae81b439b2629e3ff71c6018`  
		Last Modified: Wed, 24 Aug 2022 23:00:29 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
