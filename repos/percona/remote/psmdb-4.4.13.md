## `percona:psmdb-4.4.13`

```console
$ docker pull percona@sha256:3c3697c1840803f765f2e6af6dfec1bb4a31796f297a8668df4320a6817c6222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.13` - linux; amd64

```console
$ docker pull percona@sha256:56faa7cb555e11039ed25ead9468330dc14a7348210ac5f6677e9a741f4a4e21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.4 MB (198391432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2b459f1bc239897bc1a5a391ab8e40dbffb0f362e90d3a31559b8b9323a9d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Apr 2022 20:32:54 GMT
ADD file:2d97892bf8c2eeadd8df675df73ede6f6bc115c021f3e5c43267a14ad84f678e in / 
# Wed, 27 Apr 2022 20:32:55 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 22:11:09 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 27 Apr 2022 22:13:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 27 Apr 2022 22:13:26 GMT
ENV PSMDB_VERSION=4.4.13-13
# Wed, 27 Apr 2022 22:13:26 GMT
ENV OS_VER=el8
# Wed, 27 Apr 2022 22:13:26 GMT
ENV FULL_PERCONA_VERSION=4.4.13-13.el8
# Wed, 27 Apr 2022 22:13:26 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 27 Apr 2022 22:14:05 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 27 Apr 2022 22:14:06 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 27 Apr 2022 22:14:06 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 27 Apr 2022 22:14:07 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 27 Apr 2022 22:14:07 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Apr 2022 22:14:10 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 27 Apr 2022 22:14:12 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 27 Apr 2022 22:14:13 GMT
VOLUME [/data/db]
# Wed, 27 Apr 2022 22:14:13 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 27 Apr 2022 22:14:13 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 27 Apr 2022 22:14:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Apr 2022 22:14:14 GMT
EXPOSE 27017
# Wed, 27 Apr 2022 22:14:14 GMT
USER 1001
# Wed, 27 Apr 2022 22:14:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:79f01b38ff93019ac23e41c2714bc448edcfdd0a5bc3cc47488aa0544086e2ee`  
		Last Modified: Wed, 27 Apr 2022 20:33:41 GMT  
		Size: 87.5 MB (87481556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59739d32b88c2e95359f1db265e1fddd2e3327e7d63e5e25bd51aa1ec182eb3`  
		Last Modified: Wed, 27 Apr 2022 22:17:14 GMT  
		Size: 3.8 MB (3765191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe1b0e1146f8d4e1408b09138e63e84234c3771bbf99746e2b03d6a2122848a`  
		Last Modified: Wed, 27 Apr 2022 22:17:26 GMT  
		Size: 98.1 MB (98058644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3301754bddd9532a1fc83debd22a32d667f1ab92c71195dd3d66fc9505cde9`  
		Last Modified: Wed, 27 Apr 2022 22:17:13 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9ff4a10202eb13ea1e8803daea1f86bdbade164945ebf610159ce49a532ba`  
		Last Modified: Wed, 27 Apr 2022 22:17:13 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a453bd9a04ce1719f0bfc029402caf1cb04da9a3bbca0f2af97bd56dc5e03cc4`  
		Last Modified: Wed, 27 Apr 2022 22:17:11 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a768fce47133f313fd5382853fcfd932af47b3b7e8d9a5441e466168847ff51f`  
		Last Modified: Wed, 27 Apr 2022 22:17:11 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320592042bd9ea530b5ddc4737814a99c1e1b5ceb708bc9cc2ff93de35de6d92`  
		Last Modified: Wed, 27 Apr 2022 22:17:12 GMT  
		Size: 8.1 MB (8137885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28286f37124438e47933d65ad026486727936e3b1fce3b3ec70392920f3c5995`  
		Last Modified: Wed, 27 Apr 2022 22:17:10 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1849c0b67175d4127ae0905f91a87d1fffa3186e1a9b5ce3242191acd6f9e81f`  
		Last Modified: Wed, 27 Apr 2022 22:17:10 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
