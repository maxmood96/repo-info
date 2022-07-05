## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:ebc1f278fc12f41644ec7bc08226aa8eeaaf157eb7abaadeab1070bd11ca008e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:c8048d89460f69225cf3f10b09f3bc008919b5db799632d5e485cfe4dbac940e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176226692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532539d6af0f0571caf8a2e14de5116c5f1716b3c3c588e5e17751b950322c19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 30 Jun 2022 17:20:36 GMT
ADD file:fdf207441bdb80042fb0d3dfd9498e2bcff45ba92f9d44ab93e2596ed3bebe81 in / 
# Thu, 30 Jun 2022 17:20:37 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:56:26 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 05 Jul 2022 18:51:41 GMT
ENV PSMDB_VERSION=4.2.21-21
# Tue, 05 Jul 2022 18:51:41 GMT
ENV OS_VER=el8
# Tue, 05 Jul 2022 18:51:41 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Tue, 05 Jul 2022 18:51:42 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 05 Jul 2022 18:51:45 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Tue, 05 Jul 2022 18:52:19 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 05 Jul 2022 18:52:20 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 05 Jul 2022 18:52:20 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 05 Jul 2022 18:52:21 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 05 Jul 2022 18:52:21 GMT
ENV GOSU_VERSION=1.11
# Tue, 05 Jul 2022 18:52:24 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 05 Jul 2022 18:52:27 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 05 Jul 2022 18:52:28 GMT
VOLUME [/data/db]
# Tue, 05 Jul 2022 18:52:28 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Tue, 05 Jul 2022 18:52:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Jul 2022 18:52:28 GMT
EXPOSE 27017
# Tue, 05 Jul 2022 18:52:28 GMT
USER 1001
# Tue, 05 Jul 2022 18:52:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c36ed75e1749dabbd82d16fdd8049d3367cb86423a42f58d554c3cb1cc6ddb05`  
		Last Modified: Thu, 30 Jun 2022 17:21:22 GMT  
		Size: 84.6 MB (84570755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10226712ac893386f4a2b375ef36a69f780e80a3ad7597b66658dc22b013cd57`  
		Last Modified: Tue, 05 Jul 2022 18:53:31 GMT  
		Size: 3.7 MB (3740807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b090c7739c59a3b3838ad528f946816186b1887504f664fc84e1b81ddbab9ba4`  
		Last Modified: Tue, 05 Jul 2022 18:53:40 GMT  
		Size: 78.8 MB (78842294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec045c90fa56357e31c8c7178b0b9e9df1a025cee40e5cc7e836bb2b44eca335`  
		Last Modified: Tue, 05 Jul 2022 18:53:30 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c7916cc7088d73460cb89e7698e3136e7cd8c6087f9cf97455f1d715e9c26b`  
		Last Modified: Tue, 05 Jul 2022 18:53:28 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e900d41882472e94ca6f1464449a221ada1cd447fe810f87ae680a6ffda0f13`  
		Last Modified: Tue, 05 Jul 2022 18:53:28 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7c67bbbb01ff071fa4dba2a2aa43c53c32b5b470d6b343d8736b22db21223`  
		Last Modified: Tue, 05 Jul 2022 18:53:28 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08477f35ce3c1987915a53e3aa08d6c3960e96a0c76cc34bdb3ad81a6d8b34a`  
		Last Modified: Tue, 05 Jul 2022 18:53:29 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3315dee54eab45f85a4822376196593761dd0991feface072925b93381d39b`  
		Last Modified: Tue, 05 Jul 2022 18:53:28 GMT  
		Size: 4.6 KB (4554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
