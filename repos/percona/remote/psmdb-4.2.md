## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:12634bc7c7df47019b59712fcf644675181a7e7f83b2035fb7bb5f9555d8baa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:814ff8b4b40f6efcf5f2312620eb388fc9532d63534e6512314716c925b742dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176417396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f44b7e60ae4ac806e95f38dfaba84a7885f938040c1214778d008440ba71e6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 27 Oct 2022 17:21:34 GMT
ADD file:21d51ed5d75272951d93bd7d363ccf19173ef416b25c6acb627b575293fb7389 in / 
# Thu, 27 Oct 2022 17:21:35 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 17:45:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 27 Oct 2022 17:48:54 GMT
ENV PSMDB_VERSION=4.2.21-21
# Thu, 27 Oct 2022 17:48:55 GMT
ENV OS_VER=el8
# Thu, 27 Oct 2022 17:48:55 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Thu, 27 Oct 2022 17:48:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 27 Oct 2022 17:48:57 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Thu, 27 Oct 2022 17:49:33 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 27 Oct 2022 17:49:34 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 27 Oct 2022 17:49:34 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 27 Oct 2022 17:49:35 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 27 Oct 2022 17:49:35 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Oct 2022 17:49:38 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 27 Oct 2022 17:49:40 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 27 Oct 2022 17:49:40 GMT
VOLUME [/data/db]
# Thu, 27 Oct 2022 17:49:41 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Thu, 27 Oct 2022 17:49:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 17:49:41 GMT
EXPOSE 27017
# Thu, 27 Oct 2022 17:49:41 GMT
USER 1001
# Thu, 27 Oct 2022 17:49:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1ca7c848b9e5e4ce2ec73f5399f2b0c161b4c592c979bfb25cd1acc15ea0d84a`  
		Last Modified: Thu, 27 Oct 2022 17:23:09 GMT  
		Size: 86.0 MB (85963514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e578c0dc1ac8e9ecc6081bb4d3c9ac0c5449ee407868033f3cc054d54d919e1f`  
		Last Modified: Thu, 27 Oct 2022 17:52:28 GMT  
		Size: 3.8 MB (3773691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57510b71cf907bcf861701ff9590c4e92e105eaf3de4b8eaffe3091fca181a55`  
		Last Modified: Thu, 27 Oct 2022 17:52:37 GMT  
		Size: 77.6 MB (77607343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e5a55a11d8b8c1b54b64be293c401ab72e6a45d1badd14d3cce1db235c97df`  
		Last Modified: Thu, 27 Oct 2022 17:52:27 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba940c09c4debfdc668285ed6cb56595f4d73e23809df8d84968827300b222ef`  
		Last Modified: Thu, 27 Oct 2022 17:52:25 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa3a366de72c5b61df6c6f3c38594848012aabe504237284422045d6ec6e457`  
		Last Modified: Thu, 27 Oct 2022 17:52:25 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be74700b2a924b279dcba3766471a1aa3ff6b45f3735f23b755cfd53c0e2359b`  
		Last Modified: Thu, 27 Oct 2022 17:52:26 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593248eaf4a86295b4800a3627d1d184db507164126557b2bd5ee4563813d9`  
		Last Modified: Thu, 27 Oct 2022 17:52:27 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374fcfa5718e62753e86cd5aebce5be6306ea9fa886d426bc56fffea3eed8d9`  
		Last Modified: Thu, 27 Oct 2022 17:52:25 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
