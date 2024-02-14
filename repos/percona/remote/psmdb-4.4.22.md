## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:80a277c1b7dfc548010b846033f933e280640933d81c4d0d19bff436db86d720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:ea06d087f06615150392b66f6d8c0e98c0a6accb28b63a6533562d91fd8c6fb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250434813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790c991636a0c8a6ff7d70f7d3f2ac924a133024e71c6a7e7033fe3b5ca7d008`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:24:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:27:28 GMT
ENV PSMDB_VERSION=4.4.22-21
# Wed, 14 Feb 2024 03:27:28 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:27:28 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Wed, 14 Feb 2024 03:27:28 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:27:29 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:28:25 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:28:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:28:27 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:28:27 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:28:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:28:30 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:28:32 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:28:33 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:28:33 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:28:33 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 14 Feb 2024 03:28:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:28:33 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:28:34 GMT
USER 1001
# Wed, 14 Feb 2024 03:28:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b5634e73325442ddaf4c501f13a736a9137203641d7da275233dceeaeb02aa`  
		Last Modified: Wed, 14 Feb 2024 03:32:01 GMT  
		Size: 4.3 MB (4284783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fa19d905aa99ba03d189d271de8f76a01a350d79e076f32f19f9802bbdaf53`  
		Last Modified: Wed, 14 Feb 2024 03:33:18 GMT  
		Size: 136.3 MB (136286392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c933f44d6aac23894f5b914e5462d67c1f5f6d8e8db146a6fa29e7398f369fd9`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71366c442dfc0533125b82c245b122beb75a12e6f3038b6f3094bf3d84cba305`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b41615400a587cd4cb81cbd19927f9916727266fe6d816a3839159fd6bd26`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52de67cbb1d76190666fa4b9dd622edc7f6d3cd04c40b16be7e63c94800aa6f3`  
		Last Modified: Wed, 14 Feb 2024 03:33:00 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d829bc6a1a3eec0a7da09b157172189688cb384099d413b5e873fbefe25e0c71`  
		Last Modified: Wed, 14 Feb 2024 03:33:01 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f3832ba9b5af8c62acf1b0fbc97203fc425fa6a827d29f7bc398234b0db139`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8f4fb82711a2af6325d75404b4c995dd72754bfb1fa3a23ec84c6e3a234369`  
		Last Modified: Wed, 14 Feb 2024 03:32:59 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
