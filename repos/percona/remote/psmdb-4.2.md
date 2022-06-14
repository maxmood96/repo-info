## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:bd34e500f064ab843c19a78a0626341d26a09fcb88ab2ee34048707f43bd4043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:9a30e795404542d5acfd1054ef27dac9d5e49975c64462f01195e320ba802748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176181096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c539fe73951a9e5166e142a445f0446d52b8b53b590deeafe87a3b9c9b3234a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:16 GMT
ADD file:f0e6a328565074e88f761104e323c9f82d10f3a6835f494f792b9550d6c0780c in / 
# Tue, 14 Jun 2022 18:23:17 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:54:39 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 14 Jun 2022 18:58:15 GMT
ENV PSMDB_VERSION=4.2.20-20
# Tue, 14 Jun 2022 18:58:15 GMT
ENV OS_VER=el8
# Tue, 14 Jun 2022 18:58:15 GMT
ENV FULL_PERCONA_VERSION=4.2.20-20.el8
# Tue, 14 Jun 2022 18:58:15 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 14 Jun 2022 18:58:19 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Tue, 14 Jun 2022 18:58:54 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 14 Jun 2022 18:58:55 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 14 Jun 2022 18:58:55 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 14 Jun 2022 18:58:56 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 14 Jun 2022 18:58:56 GMT
ENV GOSU_VERSION=1.11
# Tue, 14 Jun 2022 18:58:59 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 14 Jun 2022 18:59:00 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 14 Jun 2022 18:59:01 GMT
VOLUME [/data/db]
# Tue, 14 Jun 2022 18:59:01 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Tue, 14 Jun 2022 18:59:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jun 2022 18:59:01 GMT
EXPOSE 27017
# Tue, 14 Jun 2022 18:59:01 GMT
USER 1001
# Tue, 14 Jun 2022 18:59:01 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f658974cd1e22c258b47ec713e6cfe60d8f00ec42264206a49a37bf7193cb96e`  
		Last Modified: Tue, 14 Jun 2022 18:24:03 GMT  
		Size: 84.6 MB (84562622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9718cd16b06b82ae40137e1f7acd0ae5e4da1a9c947f9aa0996f1b4e7424079a`  
		Last Modified: Tue, 14 Jun 2022 19:01:38 GMT  
		Size: 3.7 MB (3738881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29184141e9a3682ce57e8f754f9fb176419081e16ec2e983a54832f7f68bf4b`  
		Last Modified: Tue, 14 Jun 2022 19:01:47 GMT  
		Size: 78.8 MB (78806762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff10a94db28ae94ac771915f9e3e6cbcb85042e8610dd00d25d18d98229ccd10`  
		Last Modified: Tue, 14 Jun 2022 19:01:37 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73b3d09457cfcca88f30477cd91595e01a79206a015ee4dea30acba08724b27`  
		Last Modified: Tue, 14 Jun 2022 19:01:35 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbff40ecce206d4f453415dfdb0ec031f621a1a85fad6aa74044ff87f7137cc9`  
		Last Modified: Tue, 14 Jun 2022 19:01:35 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b1a2c96fa2291afd0d9341d5350074d48c0d0db87d0b1fbb8ed27cffd9237c`  
		Last Modified: Tue, 14 Jun 2022 19:01:35 GMT  
		Size: 914.5 KB (914541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dddc1ab1fc16bdf0e943be27be762cf04649ccd65c56a15152d84cb16a4f52`  
		Last Modified: Tue, 14 Jun 2022 19:01:36 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6a461a51ac583f845eca9ab4db0d3a950cabf613cf12204b9978f695c90fa3`  
		Last Modified: Tue, 14 Jun 2022 19:01:34 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
