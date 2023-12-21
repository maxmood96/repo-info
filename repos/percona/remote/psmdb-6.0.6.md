## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:ac94798e688a1a3f0209524699bb2c205665bce7168aa8f3943c00c13b8f15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:78c653fd0d857bd52d487a0421709339fa21cd9956a61a90b3e597f266dff1da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286532162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bef21bd6762406c5351fcef47dc1a3150f6e81366ddad5557cef700af28e022`
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
# Wed, 20 Dec 2023 23:19:23 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 20 Dec 2023 23:19:23 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:19:23 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 20 Dec 2023 23:19:23 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:19:23 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:20:20 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:20:22 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:20:22 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:20:23 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:20:23 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:20:26 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:20:29 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:20:29 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:20:30 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Dec 2023 23:20:30 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:20:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:20:30 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:20:30 GMT
USER 1001
# Wed, 20 Dec 2023 23:20:30 GMT
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
	-	`sha256:9a1cfb46a32b7f116e140080c70bae94ede67a054ec8ca19013a1c3f03ac9b21`  
		Last Modified: Wed, 20 Dec 2023 23:25:43 GMT  
		Size: 172.4 MB (172367277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797d4f387c0345e73df260fff0f0fcd157acf4d194e45081eef3cc2752b8f034`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cd1df821ac6601ddd4f88facccf2f8d9918eccf19d97d4fd9975487041dc26`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab79739b5162133568d02868e8474cd2a5b7a88dce69345fcb86d0978e558bbf`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c838e4c91d51625d47934536de12bdb97011d852555b715474de3ae408667a59`  
		Last Modified: Wed, 20 Dec 2023 23:25:20 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5b08c83667cd05d1ba39f3ae01f7a2e40ab1dbf1c82be4361e186d3018cb7e`  
		Last Modified: Wed, 20 Dec 2023 23:25:21 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0310c1458b09e6718a8f9419f053daac5257e3c76da0f306786c3b427951bc1`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1022828e0c9b54f5448648a480cc757451bd1a13c4c79f94c7604052c1447d3`  
		Last Modified: Wed, 20 Dec 2023 23:25:19 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
