## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:5a5c9e889081e0cac3e2116951e2a0bc8e2809262bf5c661f5776b55bbecee44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:c274ae688bf7b2f95aa14b99f54a502e5db323e30c887aef3693eb72efbcb24e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231912624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13493a7a6f4f46d289a273d9d5b8b52784c8c4395d685f2e32b736cccd871310`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:05 GMT
ADD file:043417ca603ca29472d33660c5e944bfdd4563dabf68b6e4e41a0a1a1dae8f04 in / 
# Wed, 14 Feb 2024 01:47:06 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:23:13 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:28:38 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 14 Feb 2024 03:28:38 GMT
ENV OS_VER=el8
# Wed, 14 Feb 2024 03:28:38 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 14 Feb 2024 03:28:38 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 14 Feb 2024 03:28:38 GMT
ENV PSMDB_REPO=release
# Wed, 14 Feb 2024 03:28:41 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 14 Feb 2024 03:29:36 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 14 Feb 2024 03:29:37 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 14 Feb 2024 03:29:37 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 14 Feb 2024 03:29:38 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 14 Feb 2024 03:29:38 GMT
ENV GOSU_VERSION=1.11
# Wed, 14 Feb 2024 03:29:41 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 14 Feb 2024 03:29:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 14 Feb 2024 03:29:44 GMT
VOLUME [/data/db]
# Wed, 14 Feb 2024 03:29:44 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 14 Feb 2024 03:29:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Feb 2024 03:29:44 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 03:29:44 GMT
USER 1001
# Wed, 14 Feb 2024 03:29:44 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60ccddb6218556f1d6ac035de7505a87c53b2c8653569d2a57dfc1b53c745588`  
		Last Modified: Wed, 14 Feb 2024 01:49:02 GMT  
		Size: 100.8 MB (100777076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f781da700ea39955e4ea9ec1e17f5f8437eb6ac396f642e025a076560b238c3`  
		Last Modified: Wed, 14 Feb 2024 03:33:34 GMT  
		Size: 4.3 MB (4284789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee3cbbb76419628836111775ef32c3c6f0d067128b18c9356d8d1e31242b974`  
		Last Modified: Wed, 14 Feb 2024 03:33:48 GMT  
		Size: 117.8 MB (117763846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2b5ff6f294b62e2d06e0b5c56de239bab99c067753a435fc44d1b62ea35756`  
		Last Modified: Wed, 14 Feb 2024 03:33:33 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47a4b8e9f0a803d831fe502933a1d5c981517d2d23b1401a15ba1be9fc0bd21`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a3d3b3ebfd47bf9a4ce00ae83eb845079fee1d6e0eb98c628233386aa83d57`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee85faeba83c42b64c728e732cb64e43b14d51382119724b558927e879926e9`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709167988c9838150e205539cd49e134273c668000f7c72d293342d81614cba2`  
		Last Modified: Wed, 14 Feb 2024 03:33:32 GMT  
		Size: 8.2 MB (8151449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b710d0eead90f56936c44562524a23137efcbeaf6576281ea2203eb89c42642c`  
		Last Modified: Wed, 14 Feb 2024 03:33:31 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
