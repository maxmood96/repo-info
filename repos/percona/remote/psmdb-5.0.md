## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:5a1de090b0448263cf215138cffd0d39402aa9b03490092a94e07519cc3c928a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:59155aaac905d912b1d6e98f214398a76198d90c76d9925f4a6fd3ff35d0be96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250211790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62357e193feee44d42dd47665244bc10828fa151526fb1621c30d66351c38c0`
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
# Fri, 11 Aug 2023 01:45:46 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 11 Aug 2023 01:45:46 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:45:46 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 11 Aug 2023 01:45:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:45:47 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:46:35 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:46:36 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:46:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:46:37 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:46:37 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:46:40 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:46:42 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:46:42 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:46:42 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:46:43 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:46:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:46:43 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:46:43 GMT
USER 1001
# Fri, 11 Aug 2023 01:46:43 GMT
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
	-	`sha256:9dc588820011bf0f3cde96b16eca92b7b569dc2093158ff0a32b29e5d8ffa91f`  
		Last Modified: Fri, 11 Aug 2023 01:52:00 GMT  
		Size: 148.4 MB (148405672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63425b2f2a086802849440590bb47a5888afa2ae45c5eee7aacf883a7257cef`  
		Last Modified: Fri, 11 Aug 2023 01:51:42 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bc9c20319e3fb7fdb4d3f577f1c23133effa56861776395616cefd0b870d2d`  
		Last Modified: Fri, 11 Aug 2023 01:51:42 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352941f34f632dfa06398b346dfe4c8e71dac13baf34d1a18d007c77f72f6676`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30558d227cd0bf4af5e4fb06c86b0be9c5792242f6269d963f301b435bba68b`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bda32ef50d2663304ecc3b265f024b9e41c26a9c5c73513da5e5ca71e345a16`  
		Last Modified: Fri, 11 Aug 2023 01:51:41 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2194b9ab828b8216d95f409f71b585ce9c87942284db5d0bf64ebdd2dd8105`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ed082ab48dcb8171455796e00fc80412fe87b2495e33615c934ba548deb16d`  
		Last Modified: Fri, 11 Aug 2023 01:51:40 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
