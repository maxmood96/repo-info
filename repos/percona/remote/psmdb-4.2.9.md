## `percona:psmdb-4.2.9`

```console
$ docker pull percona@sha256:211ac3322d24c940d73dc71cde1797e5bcce4384adbba9e397065c18d8dfee88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.2.9` - linux; amd64

```console
$ docker pull percona@sha256:a0296679e1e587f5bf95f213d10c740c54d896bee65b344d15909d2bdd5a7222
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169189038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c656e1d77a84e1640e7f0c9918b457519239e722a981d9ac57feed3b05a46db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Mon, 10 Aug 2020 18:43:15 GMT
LABEL org.label-schema.schema-version=1.0
# Mon, 10 Aug 2020 18:43:15 GMT
LABEL org.label-schema.name=Percona Server for MongoDB
# Mon, 10 Aug 2020 18:43:15 GMT
LABEL org.label-schema.vendor=Percona
# Mon, 10 Aug 2020 18:43:15 GMT
LABEL org.label-schema.description=Percona Server for MongoDB is our free and open-source drop-in replacement for MongoDB Community Edition. It offers all the features and benefits of MongoDB Community Edition, plus additional enterprise-grade functionality.
# Mon, 10 Aug 2020 18:43:15 GMT
LABEL org.label-schema.license=SSPLv1
# Mon, 10 Aug 2020 18:43:16 GMT
LABEL org.opencontainers.image.title=Percona Server for MongoDB
# Mon, 10 Aug 2020 18:43:16 GMT
LABEL org.opencontainers.image.vendor=Percona
# Mon, 10 Aug 2020 18:43:16 GMT
LABEL org.opencontainers.image.description=Percona Server for MongoDB is our free and open-source drop-in replacement for MongoDB Community Edition. It offers all the features and benefits of MongoDB Community Edition, plus additional enterprise-grade functionality.
# Mon, 10 Aug 2020 18:43:16 GMT
LABEL org.opencontainers.image.license=SSPLv1
# Mon, 10 Aug 2020 18:43:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 03 Sep 2020 18:25:45 GMT
ENV PSMDB_VERSION=4.2.9-9
# Thu, 03 Sep 2020 18:25:45 GMT
LABEL org.label-schema.schema-version=4.2.9-9
# Thu, 03 Sep 2020 18:25:45 GMT
LABEL org.opencontainers.image.version=4.2.9-9
# Thu, 03 Sep 2020 18:25:50 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A;     gpg --batch --keyserver pool.sks-keyservers.net --recv-keys 6341AB2753D78A78A7C27BB124C6A8A7F4A80EB5;     gpg --batch --keyserver pool.sks-keyservers.net --recv-keys 91E97D7C4A5E96F17F3E888F6A2FAEA2352C64E5;         gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 6341AB2753D78A78A7C27BB124C6A8A7F4A80EB5 > ${GNUPGHOME}/RPM-GPG-KEY-CentOS-7;     gpg --batch --export --armor 91E97D7C4A5E96F17F3E888F6A2FAEA2352C64E5 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-7;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-CentOS-7 ${GNUPGHOME}/RPM-GPG-KEY-EPEL-7;         curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Thu, 03 Sep 2020 18:25:50 GMT
ENV OS_VER=el7
# Thu, 03 Sep 2020 18:25:51 GMT
ENV FULL_PERCONA_VERSION=4.2.9-9.el7
# Thu, 03 Sep 2020 18:25:51 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 03 Sep 2020 18:25:56 GMT
RUN set -ex;     curl -Lf -o /tmp/jq.rpm https://download.fedoraproject.org/pub/epel/7/x86_64/Packages/j/jq-1.6-2.el7.x86_64.rpm;     curl -Lf -o /tmp/oniguruma.rpm https://download.fedoraproject.org/pub/epel/7/x86_64/Packages/o/oniguruma-6.8.2-1.el7.x86_64.rpm;     rpmkeys --checksig /tmp/jq.rpm /tmp/oniguruma.rpm;         rpm -i /tmp/jq.rpm /tmp/oniguruma.rpm;     rm -rf /tmp/jq.rpm /tmp/oniguruma.rpm
# Thu, 03 Sep 2020 18:26:14 GMT
RUN set -ex;     sed -i '/nodocs/d' /etc/yum.conf || :;     yum install -y         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         shadow-utils         curl         procps-ng         yum-utils;             repoquery -a --location         policycoreutils             | xargs curl -Lf -o /tmp/policycoreutils.rpm;     repoquery -a --location         percona-server-mongodb-server-${FULL_PERCONA_VERSION}             | xargs curl -Lf -o /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     rpm -iv /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm --nodeps;         rm -rf /tmp/policycoreutils.rpm /tmp/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.rpm;     yum clean all;     rm -rf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 03 Sep 2020 18:26:15 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 03 Sep 2020 18:26:15 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 03 Sep 2020 18:26:16 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server-$(echo ${FULL_PERCONA_VERSION} | cut -d - -f 1)/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 03 Sep 2020 18:26:16 GMT
ENV GOSU_VERSION=1.11
# Thu, 03 Sep 2020 18:26:19 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 03 Sep 2020 18:26:21 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 03 Sep 2020 18:26:21 GMT
COPY file:36bd7798a7bd236f79a692385b6877519fd05ff40f92de87cb1d5c527c35d799 in /entrypoint.sh 
# Thu, 03 Sep 2020 18:26:21 GMT
VOLUME [/data/db]
# Thu, 03 Sep 2020 18:26:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Sep 2020 18:26:22 GMT
EXPOSE 27017
# Thu, 03 Sep 2020 18:26:22 GMT
USER 1001
# Thu, 03 Sep 2020 18:26:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c38f44d9e5982a283b290171b58ed11c39e5df53226eadbb2985938632924f2`  
		Last Modified: Thu, 03 Sep 2020 18:26:57 GMT  
		Size: 6.5 MB (6456587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dba2f97901c267c21a0996ea8a6154bbe1693267548134b46e8b84365c628b5`  
		Last Modified: Thu, 03 Sep 2020 18:26:56 GMT  
		Size: 6.9 MB (6879924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafea5cbdbf9ae44959f7dec6483d2344b6af9e1512401b96c30e2130c5368fc`  
		Last Modified: Thu, 03 Sep 2020 18:27:05 GMT  
		Size: 70.9 MB (70914219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a6a3613f5e1a460f31cb99eac5aba827bc97d88ebce8a6ee45678dc76267ff`  
		Last Modified: Thu, 03 Sep 2020 18:26:55 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd623d0b7c60c7a205537755681b1a3df508c56e44bc4b31b2fb794cc3015b9`  
		Last Modified: Thu, 03 Sep 2020 18:26:54 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efddb325f872c593f0ffadcd76a43317f0cf086fce2fa0af1c5c3d290220e3c0`  
		Last Modified: Thu, 03 Sep 2020 18:26:54 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28e63c5a7c91f5061bed82df647bc57d3f37b0873362c902d267fc1b3a99b3`  
		Last Modified: Thu, 03 Sep 2020 18:26:54 GMT  
		Size: 915.5 KB (915465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68115486923b82c4cdb94201284ef6a8cc764408b5095bb3650aacd69e6e07a`  
		Last Modified: Thu, 03 Sep 2020 18:26:55 GMT  
		Size: 8.1 MB (8138867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eb6de4ee9ee5717585f8fc5c41d11b7e2ed24b69733e43e25bce7f3865e5e0`  
		Last Modified: Thu, 03 Sep 2020 18:26:54 GMT  
		Size: 4.5 KB (4542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
