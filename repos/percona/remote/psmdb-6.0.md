## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:05c2a1caf82b474f3dcc697e2317409e14ba612e45788156636e7e10be57c1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:dc001f31db6818d852a65dacbb6250493674eb12f47e026c0ae4a50edf57c806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286600500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b79a2b60cb90cd555517b053e154423f80c3d08ebdc0d2afb271b0586ccc2bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:51:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:51:30 GMT
ENV PSMDB_VERSION=6.0.6-5
# Thu, 09 May 2024 22:51:31 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:51:31 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Thu, 09 May 2024 22:51:31 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:51:31 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:52:29 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:52:30 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:52:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:52:31 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:52:31 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:52:35 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:52:38 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:52:38 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:52:39 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:52:39 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Thu, 09 May 2024 22:52:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:52:39 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:52:39 GMT
USER 1001
# Thu, 09 May 2024 22:52:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74628cc9f6fe7927ea24cc394193c7bd60fa9a6d344603584dadfb4b2f5722a`  
		Last Modified: Thu, 09 May 2024 22:58:36 GMT  
		Size: 4.3 MB (4297822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee38ae1140e3a8828df989148fcfb98409d849be391a106b2aed0fac581ee404`  
		Last Modified: Thu, 09 May 2024 22:58:56 GMT  
		Size: 172.4 MB (172415073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532fe1d446fddb9af95a42bfa54208e496835cf7a1bfef3967f791c2b21fd4ee`  
		Last Modified: Thu, 09 May 2024 22:58:35 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc4651397bb268cdb31c68945c59e40c3cd1b3d9951acdf57c113c3b15ec63`  
		Last Modified: Thu, 09 May 2024 22:58:35 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd05da12b796b9676cb4bc9aa4819de3860959f35cbd3fe3ebe4022a40f00ae3`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cca77b93916e911255dba27fac117176a2eff9c5237436b9458f2f6ed5661f`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d7ec866d8a821d8ec4ce4029e7fc24ee2bab43b7064d31c89686bc38065bf6`  
		Last Modified: Thu, 09 May 2024 22:58:34 GMT  
		Size: 8.1 MB (8137885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb579de012d104163b595e489034b01d55bcb8eba4cff1d4bc1f2e9d4d5170f`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf034b1c380971aea65ca491269139a78cce4fbb189e1b683f67a4f8c8b599c`  
		Last Modified: Thu, 09 May 2024 22:58:33 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
