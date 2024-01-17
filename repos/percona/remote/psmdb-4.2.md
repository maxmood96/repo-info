## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:2356ba75ee394c9a72aeaa4980e5d52d562fc76fbeb82dec7ca31c1aa643696a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:b967d8c94d2b3bcd428348bd5e996aaa767066c72b46cb440a08cc82d88cb094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231930783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c825d8de20a36962acd69548cec089b6c8233df7b5b9be68e3e4377867ba9d81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 22:00:19 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 17 Jan 2024 22:00:19 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 22:00:19 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 17 Jan 2024 22:00:19 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 22:00:19 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 22:00:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 22:01:16 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 22:01:17 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 22:01:17 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 22:01:17 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 22:01:17 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 22:01:20 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 22:01:23 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 22:01:23 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 22:01:23 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 17 Jan 2024 22:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 22:01:23 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 22:01:23 GMT
USER 1001
# Wed, 17 Jan 2024 22:01:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f632f2bd87095102ec7489275b3507016e06a1ea2cb462e9877e6188dd9186`  
		Last Modified: Wed, 17 Jan 2024 22:05:25 GMT  
		Size: 4.3 MB (4290064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4845a90d8eb1405d1ec3211d3110036a15d205f20d8fcd2b48dd2c452cee55b4`  
		Last Modified: Wed, 17 Jan 2024 22:05:40 GMT  
		Size: 117.8 MB (117768583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7571a5609c702ff5d51f9869eb97a8e5420d76fbb6b582b9e23aad0d9d6a6322`  
		Last Modified: Wed, 17 Jan 2024 22:05:24 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84b6bc9254fc6a89085a5923f8a018ca1a5e2a18ec5ecf4a158ae5fd9dde81b`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49a00c1feb8da5941a892f1362bc863e44428494cf861357eda233822480b6d`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c070b9c3f407e3b5d1b855278c8c1fee561d4d2d10cc3a4f73bffe60eeeed1ea`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315474d99ca5f5783af3ba85b780e4f424f10af0883a59b2a6022a300086651f`  
		Last Modified: Wed, 17 Jan 2024 22:05:24 GMT  
		Size: 8.2 MB (8151447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9539d5cfbbc4b099ba959d2fcb2ebbe0b4753695aaa61cac872ba3b0754f2608`  
		Last Modified: Wed, 17 Jan 2024 22:05:23 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
