## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:3ed58ce8c8fbd69f6c40f0c2f2a5391400ac0d6ad1dec38f8d0a988507f4341b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:c61c0c1f807b2f4a839695d2645487f32902dbf6392069f54952e5d94a61b700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286526471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6886eab894542f664fb16365fd78e6c669272e6f0f9f43afd566daa836e39450`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:56:37 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 17 Jan 2024 21:56:37 GMT
ENV PSMDB_VERSION=6.0.6-5
# Wed, 17 Jan 2024 21:56:37 GMT
ENV OS_VER=el8
# Wed, 17 Jan 2024 21:56:38 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Wed, 17 Jan 2024 21:56:38 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 17 Jan 2024 21:56:38 GMT
ENV PSMDB_REPO=release
# Wed, 17 Jan 2024 21:57:36 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 17 Jan 2024 21:57:38 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 17 Jan 2024 21:57:38 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 17 Jan 2024 21:57:38 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 17 Jan 2024 21:57:38 GMT
ENV GOSU_VERSION=1.11
# Wed, 17 Jan 2024 21:57:43 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 17 Jan 2024 21:57:45 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 17 Jan 2024 21:57:46 GMT
VOLUME [/data/db]
# Wed, 17 Jan 2024 21:57:46 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 17 Jan 2024 21:57:46 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Wed, 17 Jan 2024 21:57:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 21:57:47 GMT
EXPOSE 27017
# Wed, 17 Jan 2024 21:57:47 GMT
USER 1001
# Wed, 17 Jan 2024 21:57:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5469717c83d3db94c6864191ccdaadcb11e262854368aaac4bce7114ffc496`  
		Last Modified: Wed, 17 Jan 2024 22:03:45 GMT  
		Size: 4.3 MB (4290055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc784f65efa9401ff4011d96ad61843e3e829ef0684da656d50275f81fd7b891`  
		Last Modified: Wed, 17 Jan 2024 22:04:05 GMT  
		Size: 172.4 MB (172364605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ccc3bec8e8099f939588998b9513a1404208c34aa0740d98314c064426346e`  
		Last Modified: Wed, 17 Jan 2024 22:03:43 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071f0596220e5ec25a687c3d55058df77bfb28b16134d9b49ed15764dd95507a`  
		Last Modified: Wed, 17 Jan 2024 22:03:44 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33f3971df81bf288f8e208e6e7a4bd680e66af4afe884031b2f19eaebc3c3ce`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dfc925e3c4728141cdb40f74115cf372bab06f4ba051e5e431a2854aa8a7c8`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074a8e15568d9b9424d8319112f629e1bd1252eb7d29cb4388f198f3066d9074`  
		Last Modified: Wed, 17 Jan 2024 22:03:43 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48687772c3aa6fdd9acfa90e3f186062c17abdcc545ed79536c7af96f57bec1e`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de666f145043fdebef298bb8cb09c8c78e55c71be85901be57edabfdb4539cb`  
		Last Modified: Wed, 17 Jan 2024 22:03:42 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
