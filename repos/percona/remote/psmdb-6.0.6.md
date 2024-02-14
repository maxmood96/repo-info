## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:b62961d6fa30ed4fdfaa5445f28d175d240be2119d5da9feb6b073fb45669200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:a40704f86547638baf26e5f76dec951295b949f0be01bfe79ceb9398a50670df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286511320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5b6e0acd7d05e8aaf4eebff64d83ff2352ce2248601761bbf7034864118199`
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
# Wed, 14 Feb 2024 03:24:57 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 14 Feb 2024 03:24:57 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:24:57 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 14 Feb 2024 03:24:57 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:24:57 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:25:59 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:26:00 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:26:00 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:26:01 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:26:01 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:26:04 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:26:07 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:26:07 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:26:08 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 14 Feb 2024 03:26:08 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:26:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:26:08 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:26:08 GMT
USER 1001
# Wed, 14 Feb 2024 03:26:08 GMT
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
	-	`sha256:021060124ad80bd190033661eaa52f28cc0c8d2f73c8865f4e19f064ad502c5d`  
		Last Modified: Wed, 14 Feb 2024 03:32:20 GMT  
		Size: 172.4 MB (172362902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34122ae3a48402e105e6d02affaa2cc4ab29eced6bf81368ad50929e29dbb859`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79971bb90e407b13cd886932f000527230661fef66102db330bf28238bb6e6c`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef7300dbfb55a78a98561980ea5a0d6abd0d218ce3ec312597b269ba5cafc99`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0c3b7de4605dd0f7f2ed94e5b1782142c37f07bf87f3440c6b389ecf0d910d`  
		Last Modified: Wed, 14 Feb 2024 03:31:58 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0612d258b9afd71352eba793c7c12344cacf6095f74ceafcb9d3e671c11e84df`  
		Last Modified: Wed, 14 Feb 2024 03:31:59 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5cf75a2ec34bc4d09a4232e739246cc8bad8ceb9dfaaf50d0812831fd062dc`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe407e9a21d928d87b9c89c8937e97faa47ff55c9eabaf79c3d606b6c96f29d9`  
		Last Modified: Wed, 14 Feb 2024 03:31:57 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
