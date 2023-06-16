## `percona:psmdb-4.2.21`

```console
$ docker pull percona@sha256:7274d87c46dc34b972c87e2f726f2d89120ade28598215e49605e12e4f0ea38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.21` - linux; amd64

```console
$ docker pull percona@sha256:c520cd38e8e09ed9dd46f925bab730dbe938662c60ce5b9c323a40180d97720e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179355345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb7e43898b420d25f350460aed65f170899a9d7fa15ca0edbab88d6b0ea77c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 16 Jun 2023 00:20:34 GMT
ADD file:b035aa3f69efa59a3ead304859506efd235c8b26e9ce7e22ad9517c89cc50193 in / 
# Fri, 16 Jun 2023 00:20:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:45:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 16 Jun 2023 00:47:39 GMT
ENV PSMDB_VERSION=4.2.21-21
# Fri, 16 Jun 2023 00:47:39 GMT
ENV OS_VER=el8
# Fri, 16 Jun 2023 00:47:39 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Fri, 16 Jun 2023 00:47:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 16 Jun 2023 00:47:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Fri, 16 Jun 2023 00:48:21 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 16 Jun 2023 00:48:22 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 16 Jun 2023 00:48:22 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 16 Jun 2023 00:48:22 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 16 Jun 2023 00:48:22 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 00:48:25 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 16 Jun 2023 00:48:27 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 16 Jun 2023 00:48:27 GMT
VOLUME [/data/db]
# Fri, 16 Jun 2023 00:48:27 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 16 Jun 2023 00:48:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jun 2023 00:48:27 GMT
EXPOSE 27017
# Fri, 16 Jun 2023 00:48:28 GMT
USER 1001
# Fri, 16 Jun 2023 00:48:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d8b19403054493df93762a526e131edad57824e606eb5e37c358828e405ecea1`  
		Last Modified: Fri, 16 Jun 2023 00:22:00 GMT  
		Size: 88.9 MB (88875549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee973d7f327d449a2bdbac7ca72fde191b8e5831fc0623f14c8761ad07b5a5f`  
		Last Modified: Fri, 16 Jun 2023 00:50:49 GMT  
		Size: 3.8 MB (3793813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a6f7d476c8ed30b2f7749f20cd55f2c71f5424933ba277b28e085ccc34337d`  
		Last Modified: Fri, 16 Jun 2023 00:50:57 GMT  
		Size: 77.6 MB (77613137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c679223125c60fa8e32f2d37b8ef81b47145b84b2835b43906ee324e38dff8`  
		Last Modified: Fri, 16 Jun 2023 00:50:48 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80d408d14f6b48d043ee2cc9f4607644a02cb93e9466eb931b10e5bfcb7ff7b`  
		Last Modified: Fri, 16 Jun 2023 00:50:46 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92571c36686c65ed535a4681d1aa16e80e49d92f1adb98c52a1b27efedd8db90`  
		Last Modified: Fri, 16 Jun 2023 00:50:46 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a4db9b60df5279c27d256201b586fddb62b832d8257213deaa18be2cb9389`  
		Last Modified: Fri, 16 Jun 2023 00:50:47 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ede2f3b80b79b5218b5c1c88f2d93820e0aea96eedb6e299030d47420bdb7d9`  
		Last Modified: Fri, 16 Jun 2023 00:50:48 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00df84de1d5a87a4044dad63fdc0c0a57f30498f96352089f4839131f7e1525`  
		Last Modified: Fri, 16 Jun 2023 00:50:47 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
