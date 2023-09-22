## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:779f56f0241198c94d7b33b155fc4f4b35b674ac1f1a29bab7e35d4f90f24d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:9460ec2fe947374e7ab883bdbe67080b362092d2defec271cd1e78f655258c46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273673805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b584ad11c9f9a60bff571d585fc7e98496c04edb4f9ce09297aa87edcd7914`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 21 Sep 2023 23:23:50 GMT
ADD file:f1400f7c015d009a734ef72b857aca20fa0b646827d6d6c0fbd1ec44314f40f1 in / 
# Thu, 21 Sep 2023 23:23:51 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:45:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 21 Sep 2023 23:47:21 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 21 Sep 2023 23:47:21 GMT
ENV PSMDB_VERSION=6.0.6-5
# Thu, 21 Sep 2023 23:47:21 GMT
ENV OS_VER=el8
# Thu, 21 Sep 2023 23:47:21 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Thu, 21 Sep 2023 23:47:21 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 21 Sep 2023 23:47:21 GMT
ENV PSMDB_REPO=release
# Thu, 21 Sep 2023 23:48:16 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 21 Sep 2023 23:48:17 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 21 Sep 2023 23:48:17 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 21 Sep 2023 23:48:18 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 21 Sep 2023 23:48:18 GMT
ENV GOSU_VERSION=1.11
# Thu, 21 Sep 2023 23:48:21 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 21 Sep 2023 23:48:23 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 21 Sep 2023 23:48:23 GMT
VOLUME [/data/db]
# Thu, 21 Sep 2023 23:48:24 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 21 Sep 2023 23:48:24 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Thu, 21 Sep 2023 23:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Sep 2023 23:48:24 GMT
EXPOSE 27017
# Thu, 21 Sep 2023 23:48:24 GMT
USER 1001
# Thu, 21 Sep 2023 23:48:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f757f4fc3d201c5d7b9b19e3dbf0ddd78af45972be1834845cecc8fe6a2a5c27`  
		Last Modified: Thu, 21 Sep 2023 23:25:04 GMT  
		Size: 89.0 MB (88977617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4003a78974f8ca57a809c807ac3f02353b39f1aa83d1277ed078d6aa349848`  
		Last Modified: Thu, 21 Sep 2023 23:53:09 GMT  
		Size: 3.8 MB (3793031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67271601d1c396dcf71537ae7316bdee4c08e09fedebe34f880e986a480e41da`  
		Last Modified: Thu, 21 Sep 2023 23:53:30 GMT  
		Size: 171.8 MB (171816582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293cf6bb069f99067905e9f6d1150ceb395b2a447dc567c857751706f35491d3`  
		Last Modified: Thu, 21 Sep 2023 23:53:08 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6c49cbab4f13fe105e036b8ce3ab8d83fc87a847392b4075dbf8445273d4e7`  
		Last Modified: Thu, 21 Sep 2023 23:53:08 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d5759a381f0f45b82b807ed10bb647da9f14e8b67e5c12f1e7c276e2e64d5`  
		Last Modified: Thu, 21 Sep 2023 23:53:06 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a652f6040de3dae363e74292f548d1d7b5a88cad15ba012bf784172bc80efd9`  
		Last Modified: Thu, 21 Sep 2023 23:53:06 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97801fb186cc19ca4713c31fb527aea26bf936db8ae7e48d46e756acf317117`  
		Last Modified: Thu, 21 Sep 2023 23:53:08 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd665f6678bd4339b212f640456ea60a552e474c16389151eb3b1e8086cd752`  
		Last Modified: Thu, 21 Sep 2023 23:53:06 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4680872eddcccabc78ab23a921cfac3575d779bc85b30b8115a648e6156df0`  
		Last Modified: Thu, 21 Sep 2023 23:53:06 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
