## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:4db38fb39a1a8a5bad0f541e4568b3fa04d2fb0266d8fe971d3623a87783e3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:bab42bf36d1f46b791aef1f9edfc9e1e8dac2a43be21b3660eded404af3ba9ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231937861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1fda1fed8ae73f0379aff1744454071ca7133ef313d69dfa9fb09773be1927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:50:53 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 05 Apr 2024 19:50:53 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:50:54 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 05 Apr 2024 19:50:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:50:54 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:50:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:51:49 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:51:50 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:51:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:51:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:51:50 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:51:53 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:51:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:51:56 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:51:56 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:51:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:51:56 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:51:56 GMT
USER 1001
# Fri, 05 Apr 2024 19:51:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d2a44141d5dac15139bb0f28d1ce310a86fa427ed396864b7baeff18eff42f`  
		Last Modified: Fri, 05 Apr 2024 19:54:41 GMT  
		Size: 4.3 MB (4288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b644f560a7f50cdbb4e58782f763501cf0d4ef41d407a8f539a160780921d9f`  
		Last Modified: Fri, 05 Apr 2024 19:54:56 GMT  
		Size: 117.8 MB (117765835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b439ff74eea14435bf8f0d17e15be258bbcc3c498a52c5c92e829c8af9e6be9`  
		Last Modified: Fri, 05 Apr 2024 19:54:40 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120df9157f96834b7d7441651f64378902cb4b3a20e2acee37db0c66df620e8a`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be04f142be47aac9fd5d13567457bfb725e43c638d7bd93866de2f2e8d2580b`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9653537ce9c3c521b43f7565a55067de70fa9d874e5fe2526cb462fe86816462`  
		Last Modified: Fri, 05 Apr 2024 19:54:39 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f540454f6a1e1e8934421761cfc483c999b45dca64f23b47bd1590fe06db12f0`  
		Last Modified: Fri, 05 Apr 2024 19:54:40 GMT  
		Size: 8.2 MB (8151453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5721bb3989f1595f38b277a64db2c9fcc51f291bc10277d47a29e972722b3d`  
		Last Modified: Fri, 05 Apr 2024 19:54:38 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
