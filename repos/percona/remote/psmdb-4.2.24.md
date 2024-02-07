## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:ea26cc24ad333ce9fe56676ea259075086bf978d92b063c6e0284b33b146ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:e397d712b08f282ad17a8c6e2037824224caa7b7d354d3bcdde1c7ff421c10f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d022327686822f0c31fa4b94f86bb7ff6f81f38ea9018da72e1b91c6962dc2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:47:59 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 07 Feb 2024 06:47:59 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:47:59 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 07 Feb 2024 06:47:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 07 Feb 2024 06:47:59 GMT
ENV PSMDB_REPO=release
# Wed, 07 Feb 2024 06:48:02 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 07 Feb 2024 06:48:53 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 07 Feb 2024 06:48:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 07 Feb 2024 06:48:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 07 Feb 2024 06:48:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 07 Feb 2024 06:48:55 GMT
ENV GOSU_VERSION=1.11
# Wed, 07 Feb 2024 06:48:57 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 07 Feb 2024 06:48:59 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 07 Feb 2024 06:48:59 GMT
VOLUME [/data/db]
# Wed, 07 Feb 2024 06:49:00 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 07 Feb 2024 06:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Feb 2024 06:49:00 GMT
EXPOSE 27017
# Wed, 07 Feb 2024 06:49:00 GMT
USER 1001
# Wed, 07 Feb 2024 06:49:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a0b9e9b323f60e06123587564f7434c314c9d4c88fdfda35720e3283ac60a6`  
		Last Modified: Wed, 07 Feb 2024 06:52:52 GMT  
		Size: 4.3 MB (4284815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e256ffe9a34138e4c7c1ce0dcd0d046890e5337dc5f42542209b95f0c0799676`  
		Last Modified: Wed, 07 Feb 2024 06:53:07 GMT  
		Size: 117.8 MB (117771565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721f24a6becf3b86961fc631beb3e6d73aba0d7f85fd973f31fd0eb08e33ed9c`  
		Last Modified: Wed, 07 Feb 2024 06:52:50 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d06c9e4d282ee43c01ce1f7c932c4e1c3fb42f208466643ba08fc3f11f51fda`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0baab55a76002db3549569d20690cf8a4e14e513abb294081a6a7be9c63fa373`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f18540912b57be71ab04c088fbcb874600fd7dd100b19e90a90fdd49f1aa1be`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119da7b07afd289e9b848676fbce724efb65f98d0ea000e114862ef2360daa4f`  
		Last Modified: Wed, 07 Feb 2024 06:52:50 GMT  
		Size: 8.2 MB (8151455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4094cb03a3d5b98484f838abbbd039ed2fb4cc19ab200f74bf501ab0aa524842`  
		Last Modified: Wed, 07 Feb 2024 06:52:49 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
