## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:58676fc4303bdecf42b402abd31e1e85b7efc7c84986aea5ef8ea03997bcdfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:f3c24eccfe3b172846a09319f8254f085583cccf281566108978a55912c6b7f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286601164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a039a844dc9f9571f19ce5a069aaf3579dda507c01cbffa876b6041910d17c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:13:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Tue, 16 Apr 2024 20:13:08 GMT
ENV PSMDB_VERSION=6.0.6-5
# Tue, 16 Apr 2024 20:13:08 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:13:08 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Tue, 16 Apr 2024 20:13:08 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 16 Apr 2024 20:13:08 GMT
ENV PSMDB_REPO=release
# Tue, 16 Apr 2024 20:14:09 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 16 Apr 2024 20:14:10 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Tue, 16 Apr 2024 20:14:10 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 16 Apr 2024 20:14:11 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 16 Apr 2024 20:14:11 GMT
ENV GOSU_VERSION=1.11
# Tue, 16 Apr 2024 20:14:14 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 16 Apr 2024 20:14:17 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 16 Apr 2024 20:14:17 GMT
VOLUME [/data/db]
# Tue, 16 Apr 2024 20:14:18 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 16 Apr 2024 20:14:18 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Tue, 16 Apr 2024 20:14:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 20:14:18 GMT
EXPOSE 27017
# Tue, 16 Apr 2024 20:14:18 GMT
USER 1001
# Tue, 16 Apr 2024 20:14:18 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a5e0a2bb3cc381a5bdd2bea8cea5f6d155fa0c806c57d7ba868968cab01fc2`  
		Last Modified: Tue, 16 Apr 2024 20:19:12 GMT  
		Size: 4.3 MB (4297849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05d73aa4befa484597fad79fbb905cd7f103bc0dfd722218db6ed0094b1dc84`  
		Last Modified: Tue, 16 Apr 2024 20:19:33 GMT  
		Size: 172.4 MB (172415071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e716128b57e033cd653a81d513c6fc86943a623bfeebc81efc43c6cc0a70c0b`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e641f1b7f359a361bf177ca716e11afcc03f62c770f648e931c3b25cfaae5eb`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db0e924c00454605d5664d9abd47b7dfab1f575c8d5090f78a9249882d652d9`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 10.6 KB (10572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996fdd354c6335920e9f1b69e986c2690510b9a0c694e725bf042f1ed56abe3`  
		Last Modified: Tue, 16 Apr 2024 20:19:10 GMT  
		Size: 914.5 KB (914542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833df4971b3a1c37a1511aa540ff894bc12c70202608f3063f4c46e053d14fe3`  
		Last Modified: Tue, 16 Apr 2024 20:19:11 GMT  
		Size: 8.1 MB (8137884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed78326a8fa0cee7fc1fac45dcb82b8b888909bde2c128e6be977cdcce95d5a4`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4f19e572ff0cf149a63fd0bde758415002cf5abb55c7c8e4e263f22733210b`  
		Last Modified: Tue, 16 Apr 2024 20:19:09 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
