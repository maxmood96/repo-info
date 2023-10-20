## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:799d42e7a21d7f9d3b9fdec8d2b6a572e4dacc99d91acc79a03e58bcd2e3dd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:1eb76f7a23a1fa913a225b92478f465b943c2418e313b9dc25b62b15f6c01617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218145742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c79b2bdcfa189f9b5d7a7312c8307a6d416cb643e918175d39389d5181bd6d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:53:35 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 20 Oct 2023 18:53:35 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:53:35 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 20 Oct 2023 18:53:35 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:53:35 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:53:38 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:54:26 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:54:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:54:27 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:54:28 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:54:28 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:54:31 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:54:33 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:54:33 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:54:34 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:54:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:54:34 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:54:34 GMT
USER 1001
# Fri, 20 Oct 2023 18:54:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76795c0899241325dcb841525263bfd026e68ae397792bc5bbfc9d24f844036`  
		Last Modified: Fri, 20 Oct 2023 18:58:34 GMT  
		Size: 3.8 MB (3797333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1636e9f4b2007a174616e0afcaa4483df12d019137b556fd6f597508ed89c1`  
		Last Modified: Fri, 20 Oct 2023 18:58:48 GMT  
		Size: 117.3 MB (117257972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbd71f3c4c238975cf62751c23db53c57a6305c654d6d8fa92ea85103dc69a2`  
		Last Modified: Fri, 20 Oct 2023 18:58:33 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b324880d43da00be84772170373031e04f83e8968d30558c39b43a00686f5504`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a45ce4781f928b7d7a708774c9a1413a06ef2d4834cfe160173c28e89fcbb2`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5158a8bd7b1882440261d387042b11f1edb14d3822490dab2df05d66d732017e`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f665c9c567a036881bb25a0750636f87264ca52434e43d8cca0f0ff228081f`  
		Last Modified: Fri, 20 Oct 2023 18:58:32 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958128413188fd5a6a1d46e2692b1ad8d0e18328aa08d35c69dca8ec24bdfe9`  
		Last Modified: Fri, 20 Oct 2023 18:58:31 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
