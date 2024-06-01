## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:c0b020618a09dc45863e88b04cd73752f9c14264fc0c03d3abd3f8bf1558b446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:3e39c5a0e1ac3cd30ea72fc53b838704bf9d7c7142b689a527fb0e35ecad970c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262943048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e81e779d413b7e8ce0508054daa235ae20bcb515101ba78c5c5d8184095a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:40:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:41:55 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 01 Jun 2024 01:41:55 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:41:55 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 01 Jun 2024 01:41:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:41:55 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:42:52 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:42:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:42:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:42:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:42:54 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:42:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:43:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:43:01 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:43:02 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 01 Jun 2024 01:43:02 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:43:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:43:02 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:43:02 GMT
USER 1001
# Sat, 01 Jun 2024 01:43:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3bd182f766d84adb9d6a9fb3354c19a49292e916414fba6542e8dcf0e2a5b`  
		Last Modified: Sat, 01 Jun 2024 01:47:46 GMT  
		Size: 4.3 MB (4284324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a97f1b5cc25edef1d5b526a423e078f6807d807e3093fa89e53d71520c5243`  
		Last Modified: Sat, 01 Jun 2024 01:48:35 GMT  
		Size: 148.9 MB (148885063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d6a1f0c59dc00478baf0d3722d7e8b878faedfcffb44eed7c444bc961eba68`  
		Last Modified: Sat, 01 Jun 2024 01:48:17 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bc2875cdd31896903b89eb3c408137e935f68b6f4aab0738f5c31ea36cc36d`  
		Last Modified: Sat, 01 Jun 2024 01:48:17 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b2ef585751ffe86c9abf2036e79b3662f8211e45c1f8d6328a27a94aafc456`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0b7ab7f1ab43343275b195b09b2190ae4fd99811725aa5279a5fb966bbc0df`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 914.5 KB (914540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203498c21995eebfeb5168b2efafb723daa8740d2b2b694403b72f4c0fa7ddb2`  
		Last Modified: Sat, 01 Jun 2024 01:48:16 GMT  
		Size: 8.1 MB (8137897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88455981b7aea57ba97fc18d19a74382b9fd56c5a4bc7712fbc5adbf4c92279`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c34f5780bbfb18aa44954dc54dbe5b526ba14564e052d993c9800b93492a04d`  
		Last Modified: Sat, 01 Jun 2024 01:48:15 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
