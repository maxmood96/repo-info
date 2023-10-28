## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:f02537d06a9635684ed241534720ef741be056cbf3d61b4f116bf6583597321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:8d6ab72c7cf21df79f80d6d25b299f7d268cc92ef4e773051116b5ff3eb5f1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272703734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b6583aaef0c92ce88a1fdbe8145fa19df67d2cc517cbde2ad84298e2e506cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:49:46 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:49:46 GMT
ENV PSMDB_VERSION=6.0.6-5
# Sat, 28 Oct 2023 03:49:46 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:49:47 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Sat, 28 Oct 2023 03:49:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:49:47 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:50:40 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:50:41 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:50:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:50:42 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:50:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:50:46 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:50:48 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:50:48 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:50:49 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:50:49 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:50:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:50:49 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:50:49 GMT
USER 1001
# Sat, 28 Oct 2023 03:50:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eeb0ac3cb824b62462de95bf0bacf0c845c5f1cc41f3b946df133848e07d`  
		Last Modified: Sat, 28 Oct 2023 03:55:38 GMT  
		Size: 3.8 MB (3787490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8333bc9d3ee05bf48946f358d4d89fb102321d07b97ebb6b3358e5e232e35e58`  
		Last Modified: Sat, 28 Oct 2023 03:55:57 GMT  
		Size: 171.8 MB (171824816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4354fe6b0af06cec52bdba082495e28d69c2ea57029f41174a320d08294a6dae`  
		Last Modified: Sat, 28 Oct 2023 03:55:37 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee71068ca0cd8a1a1f1c08f0b09a9d97060be2f6a15c863fe3dccc6f64ecedf1`  
		Last Modified: Sat, 28 Oct 2023 03:55:37 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9946914dda692502f637e87722e8d95a3a28232493fdc7071063e5107da0ca51`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16953c45b3a1409e51afae93764deace18b0dc66b6b7f535f75d47eb4c972fc`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d922cf67c7ae1a995d7a0eab5101fe6670f5d18b64caa3ec7052c9722617100`  
		Last Modified: Sat, 28 Oct 2023 03:55:36 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329ec53cf21ca808e7eaf6c8b97ead7b4703118e24651f104b52deb852f4b79a`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a864e6ad90b15619737435bf369e6a4faad4369ac104f2e85851778987a383`  
		Last Modified: Sat, 28 Oct 2023 03:55:35 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
