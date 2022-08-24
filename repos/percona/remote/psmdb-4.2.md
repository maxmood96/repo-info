## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:db4d4ff2933910b7f1688d80a58fbd71210bc56cc839392f9312290e79087c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:c90e702ef71513b3c63379ca737f56f3f473bd9042fcc23c3d458572027239a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175241756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18f3693bc48813e29c117c6a1223a9014e38ec4ff5acd33e1ca60bd29211011`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:07 GMT
ADD file:9a374ea666c7366668418b8af9d065177ddb8d6d06c691efd448c1782a7202bf in / 
# Wed, 24 Aug 2022 19:35:08 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 22:54:19 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 24 Aug 2022 22:57:34 GMT
ENV PSMDB_VERSION=4.2.21-21
# Wed, 24 Aug 2022 22:57:34 GMT
ENV OS_VER=el8
# Wed, 24 Aug 2022 22:57:34 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Wed, 24 Aug 2022 22:57:34 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 24 Aug 2022 22:57:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Wed, 24 Aug 2022 22:58:11 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 24 Aug 2022 22:58:12 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 24 Aug 2022 22:58:12 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 24 Aug 2022 22:58:12 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 24 Aug 2022 22:58:12 GMT
ENV GOSU_VERSION=1.11
# Wed, 24 Aug 2022 22:58:15 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 24 Aug 2022 22:58:17 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 24 Aug 2022 22:58:17 GMT
VOLUME [/data/db]
# Wed, 24 Aug 2022 22:58:17 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 24 Aug 2022 22:58:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Aug 2022 22:58:17 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:58:17 GMT
USER 1001
# Wed, 24 Aug 2022 22:58:17 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:aaa7eee1c5ce4029df4c0919904d64a8ee908a0d06ce6618fcb69158082582bf`  
		Last Modified: Wed, 24 Aug 2022 19:36:47 GMT  
		Size: 84.9 MB (84857067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2edebb32d99158591625baa1a9ec459d4a1e3c2e82676eacf5648718650c95`  
		Last Modified: Wed, 24 Aug 2022 23:00:57 GMT  
		Size: 3.7 MB (3744779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedf0842715903384f4c94bf6086d450ced1d979014369bdcdbfa5e7ffde069b`  
		Last Modified: Wed, 24 Aug 2022 23:01:07 GMT  
		Size: 77.6 MB (77567072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08200b8af5aa30a8b1a2780dce37f0b9d5bce1e9b736c1d8b71daed5c7a07a06`  
		Last Modified: Wed, 24 Aug 2022 23:00:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d378b8e3455c03a2975de0199676c87a67afa1e0f71d55f289a27da0eecd7ca`  
		Last Modified: Wed, 24 Aug 2022 23:00:54 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d93cfb66659567a73a744da8e1a9e6eeccc78cbdb769c8a61ce61befadf6fc`  
		Last Modified: Wed, 24 Aug 2022 23:00:54 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997f6a29be72b0edc6ee2ac7caa1f89a0ad700063b708b2f9360b8459d91c9c0`  
		Last Modified: Wed, 24 Aug 2022 23:00:54 GMT  
		Size: 914.5 KB (914548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1a2b3dbe62e39460d1896ff155aeab79bd657a2c82d8d37474bcf3bef21f6`  
		Last Modified: Wed, 24 Aug 2022 23:00:55 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e76dc73ebb8d409bc16d68e33bb04c0bc44635b7d9efe732c55686adc0fab2`  
		Last Modified: Wed, 24 Aug 2022 23:00:54 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
