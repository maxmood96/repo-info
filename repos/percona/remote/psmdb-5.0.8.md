## `percona:psmdb-5.0.8`

```console
$ docker pull percona@sha256:b0e4960aa83f0abbe35eba95447d0cf95a792a4a1bc7377a44b9f500fdd1e7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.8` - linux; amd64

```console
$ docker pull percona@sha256:3cd0d079832291d0e6f2ce2d412af0c70180ecd9fb270ddf9e381d701b46f119
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210804198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12005946df7cdc017ad235ec1c2fc8b4ead1c4131863a181a773134156653775`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 May 2022 22:41:30 GMT
ADD file:eafd9e49bc2d45c1c5bf5571be43743e0500886224b81c0a07dc7c3d1702d7bb in / 
# Tue, 17 May 2022 22:41:30 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:13:01 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 May 2022 23:14:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Tue, 17 May 2022 23:14:33 GMT
ENV PSMDB_VERSION=5.0.8-7
# Tue, 17 May 2022 23:14:33 GMT
ENV OS_VER=el8
# Tue, 17 May 2022 23:14:33 GMT
ENV FULL_PERCONA_VERSION=5.0.8-7.el8
# Tue, 17 May 2022 23:14:33 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 May 2022 23:15:16 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 17 May 2022 23:15:17 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 17 May 2022 23:15:17 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 17 May 2022 23:15:18 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 17 May 2022 23:15:18 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 May 2022 23:15:21 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 17 May 2022 23:15:24 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 17 May 2022 23:15:24 GMT
VOLUME [/data/db]
# Tue, 17 May 2022 23:15:25 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 17 May 2022 23:15:25 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Tue, 17 May 2022 23:15:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 May 2022 23:15:25 GMT
EXPOSE 27017
# Tue, 17 May 2022 23:15:25 GMT
USER 1001
# Tue, 17 May 2022 23:15:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:25cd53f41add30fe2e87a488316e4bcfbecf123077c0f9f29be5cd359cbafd32`  
		Last Modified: Tue, 17 May 2022 22:42:23 GMT  
		Size: 84.6 MB (84569034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e97afd301adb5b4a617ddce810f7c4e0ca216af995248a78c29c5f15c8a1c17`  
		Last Modified: Tue, 17 May 2022 23:19:19 GMT  
		Size: 3.7 MB (3745454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7864fc6bed341635564255904de9cddc38490e216519dd8e94cff28c2d6fc60b`  
		Last Modified: Tue, 17 May 2022 23:19:32 GMT  
		Size: 113.4 MB (113403662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807db45be1d363192bc4352c9a33634821bf4a6e38356c2b3535dcdbebb6cf8`  
		Last Modified: Tue, 17 May 2022 23:19:18 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba9e3341ee8da3ffdbf73c280609b9dc9d6382db1148c3c693fbec8c95ae8bb`  
		Last Modified: Tue, 17 May 2022 23:19:18 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f000c99a2ecc19b27f6339e41164dbb8294b2baaaa18337afddde5bc08a63c3`  
		Last Modified: Tue, 17 May 2022 23:19:15 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb31f48faffef9b952318d3b1bf41ecf31e2b37dc1750ab618e9414deabcd89`  
		Last Modified: Tue, 17 May 2022 23:19:16 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646b54851678e5097e8901249faeff3a95ac39c39ead2c00e7cd5d2b39fb2ad`  
		Last Modified: Tue, 17 May 2022 23:19:17 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5244c0041101b558b644a60522db4ded43634551f6de601836f47b31f1ce8a3`  
		Last Modified: Tue, 17 May 2022 23:19:15 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29148cdf65e3e1b512bbdb5a4d8ef8e8b78b12798b746e27da11808ee4c7b300`  
		Last Modified: Tue, 17 May 2022 23:19:15 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
