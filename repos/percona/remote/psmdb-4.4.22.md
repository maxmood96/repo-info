## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:4e71e7839bda28a725251414f385e8d6391bb4d41a706d4bd7a601b7b7faf52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:7c52eee26ff412ecb3969702bebfc5d69b30d662ec4e05f0a2a026ca61ca3f6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236661972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a979a1c9b8b0942e8274d850ed68b05cfaef5c36f19f765ce088c3882985391`
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
# Sat, 28 Oct 2023 03:52:04 GMT
ENV PSMDB_VERSION=4.4.22-21
# Sat, 28 Oct 2023 03:52:04 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:52:04 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Sat, 28 Oct 2023 03:52:04 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:52:04 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:52:53 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:52:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:52:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:52:55 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:52:55 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:52:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:52:59 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:52:59 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:53:00 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:53:00 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Sat, 28 Oct 2023 03:53:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:53:00 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:53:00 GMT
USER 1001
# Sat, 28 Oct 2023 03:53:00 GMT
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
	-	`sha256:901eb5560838581fe3fce62b3efdef0fee4308c62952ab1fa784ccf850d4fbe1`  
		Last Modified: Sat, 28 Oct 2023 03:56:54 GMT  
		Size: 135.8 MB (135783073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e93c997c7436b089aee1ff21a7046993db82e76be1f473bca8ef1081e20bb87`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc2ddf356b06d5c0ced8bc092ed85ec13ee2a80b22dc0902567b93a144814d`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ca40975bfce537fd3ba2afaafa8b7f4466f7b0618397e64e81002c4722bec0`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626c15e195538af552f994c1480521353f448dc299a37bc02898b6ff293092bc`  
		Last Modified: Sat, 28 Oct 2023 03:56:36 GMT  
		Size: 914.5 KB (914543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499ff487a177f0b835f47e8e9b11e215551a3b343b9efeba653a0207b0020d0b`  
		Last Modified: Sat, 28 Oct 2023 03:56:37 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a554d2942b045fa604731729991c6082011f49fe29bb73a6b9f8a36fbf3cf8`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77309a77b170f62ef51c0cb3f30115c328c88ae314117ef4b63f5b8d3cdd7d5a`  
		Last Modified: Sat, 28 Oct 2023 03:56:35 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
