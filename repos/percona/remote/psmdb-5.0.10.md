## `percona:psmdb-5.0.10`

```console
$ docker pull percona@sha256:6cf1daefc0c4b492bbf096075260206743c744793da9fb3c001e2a7849e09171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.10` - linux; amd64

```console
$ docker pull percona@sha256:8ccfbdfe50647a7f3204ee0fb5f52e8f7ecf54150b79f18c5a74320d30307373
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (209953339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c9a08e65370ec1004d247c24bd3c425abc4cdf2fad20c8e0440b200f29d057`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:07 GMT
ADD file:9a374ea666c7366668418b8af9d065177ddb8d6d06c691efd448c1782a7202bf in / 
# Wed, 24 Aug 2022 19:35:08 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 22:54:19 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 24 Aug 2022 22:55:50 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 24 Aug 2022 22:55:50 GMT
ENV PSMDB_VERSION=5.0.10-9
# Wed, 24 Aug 2022 22:55:50 GMT
ENV OS_VER=el8
# Wed, 24 Aug 2022 22:55:50 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Wed, 24 Aug 2022 22:55:50 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 24 Aug 2022 22:56:27 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 24 Aug 2022 22:56:28 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 24 Aug 2022 22:56:29 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 24 Aug 2022 22:56:29 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 24 Aug 2022 22:56:29 GMT
ENV GOSU_VERSION=1.11
# Wed, 24 Aug 2022 22:56:33 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 24 Aug 2022 22:56:36 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 24 Aug 2022 22:56:36 GMT
VOLUME [/data/db]
# Wed, 24 Aug 2022 22:56:37 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 24 Aug 2022 22:56:37 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 24 Aug 2022 22:56:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Aug 2022 22:56:37 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:56:37 GMT
USER 1001
# Wed, 24 Aug 2022 22:56:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:aaa7eee1c5ce4029df4c0919904d64a8ee908a0d06ce6618fcb69158082582bf`  
		Last Modified: Wed, 24 Aug 2022 19:36:47 GMT  
		Size: 84.9 MB (84857067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a92fe27775b90d6c009b0e4abfaa66aa35c1a65d5b9ebb8eb6dd0ef0c3bcbc`  
		Last Modified: Wed, 24 Aug 2022 23:00:06 GMT  
		Size: 3.7 MB (3744843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64c9b959d4fd78eefce41d4c2ef86e174730d403fb30d69aeb4abada68c4ad9`  
		Last Modified: Wed, 24 Aug 2022 23:00:19 GMT  
		Size: 112.3 MB (112265380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3be505ed70cd62af41109a41c5d66a2f5c17503e48712ed163b1bade1ec3b64`  
		Last Modified: Wed, 24 Aug 2022 23:00:05 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98430d2136bc745bc0ff285faf89a342bf761615abf7fa977caa88732965fc04`  
		Last Modified: Wed, 24 Aug 2022 23:00:04 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59a290b779c01e63f1a66f41ecbcdfed66a43727bac3c75db4b513caca413f3`  
		Last Modified: Wed, 24 Aug 2022 23:00:02 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3199f7470eca6167431de3d89bacae508b28e01d48da97370842bcd04e34062d`  
		Last Modified: Wed, 24 Aug 2022 23:00:02 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7e2648dff0f301d10da4a221b9f656790e753ba7ba0b7185bcf106c1cf60cb`  
		Last Modified: Wed, 24 Aug 2022 23:00:04 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59abcc7d42ad086e4c160c9b270d3a5956d1b455e0656345364ae9522180c8d4`  
		Last Modified: Wed, 24 Aug 2022 23:00:02 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2f7cfe072604630409e5f77ee46a37121267e3a3618ed9ddc39caf8566ad5b`  
		Last Modified: Wed, 24 Aug 2022 23:00:02 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
