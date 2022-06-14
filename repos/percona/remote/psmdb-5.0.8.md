## `percona:psmdb-5.0.8`

```console
$ docker pull percona@sha256:a44ab512a6878d9f0902ff4636e2399ce5e2c06fd7f1d2df92531ad325d0ac45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.8` - linux; amd64

```console
$ docker pull percona@sha256:5c8b7828f44a541a85e2e902b200a68f59be1bf9b4a5f319ae9e0c564b2a997f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210776137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ea1493d8b0c9bf46b9eb9f3c26f209e83b49e337f3a8a71645f10737251c6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:16 GMT
ADD file:f0e6a328565074e88f761104e323c9f82d10f3a6835f494f792b9550d6c0780c in / 
# Tue, 14 Jun 2022 18:23:17 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:54:39 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 14 Jun 2022 18:56:11 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Tue, 14 Jun 2022 18:56:11 GMT
ENV PSMDB_VERSION=5.0.8-7
# Tue, 14 Jun 2022 18:56:11 GMT
ENV OS_VER=el8
# Tue, 14 Jun 2022 18:56:11 GMT
ENV FULL_PERCONA_VERSION=5.0.8-7.el8
# Tue, 14 Jun 2022 18:56:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 14 Jun 2022 18:57:03 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 14 Jun 2022 18:57:04 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 14 Jun 2022 18:57:04 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 14 Jun 2022 18:57:04 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 14 Jun 2022 18:57:04 GMT
ENV GOSU_VERSION=1.11
# Tue, 14 Jun 2022 18:57:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 14 Jun 2022 18:57:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 14 Jun 2022 18:57:12 GMT
VOLUME [/data/db]
# Tue, 14 Jun 2022 18:57:13 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 14 Jun 2022 18:57:13 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Tue, 14 Jun 2022 18:57:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jun 2022 18:57:13 GMT
EXPOSE 27017
# Tue, 14 Jun 2022 18:57:13 GMT
USER 1001
# Tue, 14 Jun 2022 18:57:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f658974cd1e22c258b47ec713e6cfe60d8f00ec42264206a49a37bf7193cb96e`  
		Last Modified: Tue, 14 Jun 2022 18:24:03 GMT  
		Size: 84.6 MB (84562622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48518af5f057cf51636bd9c9c6ece0ac01ee2af5ac4e654759222730eb51144`  
		Last Modified: Tue, 14 Jun 2022 19:00:46 GMT  
		Size: 3.7 MB (3738879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3f6ecf7664766c334aefe0eacdd82730c762a9d25d34975ee732427268f1`  
		Last Modified: Tue, 14 Jun 2022 19:00:59 GMT  
		Size: 113.4 MB (113388598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1aa2bd83afbc902c828e9fc9820c16da69c014f7fde233d5fe38f3ca8cfbe5`  
		Last Modified: Tue, 14 Jun 2022 19:00:45 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3058d2c6d0daa1c8d876fdd02f02eba5c303e287a2f508323d3adedd71b7ae`  
		Last Modified: Tue, 14 Jun 2022 19:00:45 GMT  
		Size: 4.1 KB (4098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c95851320cdeeaa2659e2fc69b756aabde72adf5c7f810eeda5de95d08902a`  
		Last Modified: Tue, 14 Jun 2022 19:00:43 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62022f4a68ce17e220f01889e36d348f8c156e8a6ef65a652a6ec9e52ceb921b`  
		Last Modified: Tue, 14 Jun 2022 19:00:43 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad089e82497b16558c5e7c2785b3c470c77254e494e8d6b9a68940d3b91320c`  
		Last Modified: Tue, 14 Jun 2022 19:00:44 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b9ebc04f07783b79ee13ef057c7f5a2b58dc60e02d97876e5d8c459010f67b`  
		Last Modified: Tue, 14 Jun 2022 19:00:42 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6e6eced950a81fa876f558972cf2f809aa3df20103f444a1ec825fbfce20b9`  
		Last Modified: Tue, 14 Jun 2022 19:00:42 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
