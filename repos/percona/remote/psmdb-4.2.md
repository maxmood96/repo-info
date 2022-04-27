## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:0542205b124842fbb9afb1c5bed31ca53a288ffb633d7d9b5777f9fe747ed3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:453a0b2e6491e0456bb67b989da6ae42524fc7b0f1bcc0cf244ae170f363e66c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179117311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4174af1087bcd820a77e58bcb35c7239d645a92b643300b95c1705f279cc87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Apr 2022 20:32:54 GMT
ADD file:2d97892bf8c2eeadd8df675df73ede6f6bc115c021f3e5c43267a14ad84f678e in / 
# Wed, 27 Apr 2022 20:32:55 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 22:11:09 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 27 Apr 2022 22:14:20 GMT
ENV PSMDB_VERSION=4.2.19-19
# Wed, 27 Apr 2022 22:14:20 GMT
ENV OS_VER=el8
# Wed, 27 Apr 2022 22:14:20 GMT
ENV FULL_PERCONA_VERSION=4.2.19-19.el8
# Wed, 27 Apr 2022 22:14:20 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 27 Apr 2022 22:14:24 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Wed, 27 Apr 2022 22:14:59 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 27 Apr 2022 22:15:00 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 27 Apr 2022 22:15:00 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 27 Apr 2022 22:15:01 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 27 Apr 2022 22:15:01 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Apr 2022 22:15:04 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 27 Apr 2022 22:15:05 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 27 Apr 2022 22:15:05 GMT
VOLUME [/data/db]
# Wed, 27 Apr 2022 22:15:05 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 27 Apr 2022 22:15:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Apr 2022 22:15:06 GMT
EXPOSE 27017
# Wed, 27 Apr 2022 22:15:06 GMT
USER 1001
# Wed, 27 Apr 2022 22:15:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:79f01b38ff93019ac23e41c2714bc448edcfdd0a5bc3cc47488aa0544086e2ee`  
		Last Modified: Wed, 27 Apr 2022 20:33:41 GMT  
		Size: 87.5 MB (87481556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90ee289e9441b2db11bfef8f623dfa0f93bc39de4f67aafad7805d7444b7505`  
		Last Modified: Wed, 27 Apr 2022 22:17:39 GMT  
		Size: 3.8 MB (3765215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680cb4699b8821bf23d04508e5af3a76a08b7782ed2f6b3d57bd70676a76c3cf`  
		Last Modified: Wed, 27 Apr 2022 22:17:48 GMT  
		Size: 78.8 MB (78797704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6374f2ec1181c25e7df4529f9a5ba58a6bf24e2cbcd9f15523637128a7ba90f5`  
		Last Modified: Wed, 27 Apr 2022 22:17:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1526bb1d750967ac98e9ff3308a7549ad5e67d4d17f832a76f6cc32e96ef5239`  
		Last Modified: Wed, 27 Apr 2022 22:17:36 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6086cc03d0b02715fe8c219399df01149498579b7d5b7e5487d2508772b9efbd`  
		Last Modified: Wed, 27 Apr 2022 22:17:36 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c30f11da0f2b31b5f86bddd186bc7ae08823951f5d8b5cc90c3afcfe06857a`  
		Last Modified: Wed, 27 Apr 2022 22:17:36 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9b80736f8b41f415457e136f6283ddec6c15555e65744fc6529b1a4ff2b19`  
		Last Modified: Wed, 27 Apr 2022 22:17:38 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae40b45675e99eb850dad01cf8574e5048ad1c7df5850d55912645b0847db0`  
		Last Modified: Wed, 27 Apr 2022 22:17:36 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
