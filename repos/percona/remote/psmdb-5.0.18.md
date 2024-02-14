## `percona:psmdb-5.0.18`

```console
$ docker pull percona@sha256:e726939332e2dae90eff882c0a1c90eecbb14db8288649fda6b631a4070e13d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.18` - linux; amd64

```console
$ docker pull percona@sha256:8089f9e18d0c055beb51984c9cedeb1a50f284f3ad89fe6cab2630a6e810d30f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263043504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765607bcb8e87b7ad0471ca366da2bae2766dc47b98ae74238d4d0cffbba649e`
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
# Wed, 14 Feb 2024 03:26:18 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 14 Feb 2024 03:26:18 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:26:18 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 14 Feb 2024 03:26:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:26:18 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:27:17 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:27:18 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:27:18 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:27:19 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:27:19 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:27:22 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:27:24 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:27:24 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:27:25 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:27:25 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:27:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:27:25 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:27:25 GMT
USER 1001
# Wed, 14 Feb 2024 03:27:25 GMT
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
	-	`sha256:dc5fff3254479387f2542bbf5b9e32b0ed20c5c6b650fd0bb9373ff1c0d81deb`  
		Last Modified: Wed, 14 Feb 2024 03:32:50 GMT  
		Size: 148.9 MB (148895087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addcec4c3400336e13aedc295a8c60e3af45c1beabde402f808527973eb5f419`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deb95d882df26ca2ec93d6aca72133408caa6c2188c5390cf7aac73e1a3e5e8`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42197984ee26fef93e92f7fb541ccb6159c85dc6ab4db6fd28fc97397696d5b2`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac12d2cbb4f0db619a1e20221ba2c242bf9a959f6838d77cf739bc43d4e1bc1`  
		Last Modified: Wed, 14 Feb 2024 03:32:31 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aab4c6450b63153888c1b2bef0daca57ea7ac840adbac952362b07b3edf657`  
		Last Modified: Wed, 14 Feb 2024 03:32:32 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417b6e04893106d0c9c0eb8aee46c068ae2d8fd1d0332b64345340e7dd10a1cd`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee85fc0166b1f4d18cb07ca260ae4014bd6454b998d4796bec7599aacfcc4ab`  
		Last Modified: Wed, 14 Feb 2024 03:32:30 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
