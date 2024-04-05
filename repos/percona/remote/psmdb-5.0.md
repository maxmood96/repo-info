## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:38757ba32542991d0e39e9d6ff24fbda29e51f230f324678501487787b36bdf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:5f297468279b297be9f85b744865d3b9c0c7ed310518423d4690e3fa4bdf2828
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263074402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227e545ad8b2f3a48f9b4f7cce0858dd77277a227bc4565a6da5d58941b62105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:48:33 GMT
ENV PSMDB_VERSION=5.0.18-15
# Fri, 05 Apr 2024 19:48:33 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:48:33 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Fri, 05 Apr 2024 19:48:33 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:48:33 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:49:29 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:49:30 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:49:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:49:31 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:49:31 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:49:34 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:49:36 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:49:36 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:49:36 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:49:37 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:49:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:49:37 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:49:37 GMT
USER 1001
# Fri, 05 Apr 2024 19:49:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc1c5a5d8764f1bae0e6f9cb85623ad7d7dc5dc86f7c362363a0eec133a960`  
		Last Modified: Fri, 05 Apr 2024 19:54:00 GMT  
		Size: 148.9 MB (148902725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc280794bd1d369744e8fdc4e159b80cbee5c6834b8e79b0c89fa5b90cf1da86`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b53458941f4cfbc5e3cfaa1bbbc48e3650f4f80da3e2659045e814d1d46c63b`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b6833b960d7b4ca7de8e5635a96183fd3d23f599e6ff177b99324eb14174a0`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74451a5de30ed5ea18d21fecfeaed975e141fdeee092765dfb49905aeaf0eb1a`  
		Last Modified: Fri, 05 Apr 2024 19:53:41 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a2759586cac3dc57d8ab09e45b8c50a26374d51d1d041fbe5f0061dcfceb8`  
		Last Modified: Fri, 05 Apr 2024 19:53:42 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02922457eb36f02de272c19413fbb3acf907396c713ae7ac647cbe35f3d3182b`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd67c841a9e9e53ccd428bdefaa4fedc10e5605d630ed8d53aec23a313f513f`  
		Last Modified: Fri, 05 Apr 2024 19:53:40 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
