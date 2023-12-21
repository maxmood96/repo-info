## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:70815eb28601ea64bf26fe10e44aefe21f63aeb2a05067a58a9457ffc163d9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:8adb46090f8725e72bdeef28d32d59cb5d9e3c9fd208de1dd389f706c2a49ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263055134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c12793e251586d3ec640a6b154248096327533e3c0122d383c3f6a5e237ccf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:19:22 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:20:43 GMT
ENV PSMDB_VERSION=5.0.18-15
# Wed, 20 Dec 2023 23:20:43 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:20:43 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Wed, 20 Dec 2023 23:20:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:20:43 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:21:39 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:21:40 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:21:40 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:21:41 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:21:41 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:21:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:21:46 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:21:47 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:21:47 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Dec 2023 23:21:47 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:21:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:21:47 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:21:48 GMT
USER 1001
# Wed, 20 Dec 2023 23:21:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e099ce6dbe00ffad7ca87f30f23228820dc3cb34aa6c6ae16b66095ca55e2`  
		Last Modified: Wed, 20 Dec 2023 23:25:22 GMT  
		Size: 4.3 MB (4293704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507ad04f12bc98662f152950972d761ce282519815a59132dec61b4f96de24c7`  
		Last Modified: Wed, 20 Dec 2023 23:26:14 GMT  
		Size: 148.9 MB (148890251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba97b3d77c782017bf9c3471a6131a76b243b3ea66d3cc8d7ea0703c461c170`  
		Last Modified: Wed, 20 Dec 2023 23:25:55 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601453f10a5c6118ab5f86a2a6eb8050463de3d60a76dd3367b43e28f70d1eb5`  
		Last Modified: Wed, 20 Dec 2023 23:25:55 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4017d4aec5d279b15c8b11c6e851678cf75e966ae5afe8b4429a6e388250010e`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43d69aad92641bbb56efe2a9a00636aaed595762ab8628d09b19c694b3a7db`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ece106b3b8646f991a0d770aa326708ee85be2e854cef830407e8b79b1568cf`  
		Last Modified: Wed, 20 Dec 2023 23:25:54 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398eb3641f6a7fc57809d9ff6dd1603c75a49adc789f8cd17cb78a484f8fbb1a`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760bed2f1396884ac9ded362d1e39aeef9b1cb71d366bbd9e6cf75126424587f`  
		Last Modified: Wed, 20 Dec 2023 23:25:53 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
