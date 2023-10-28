## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:efc61ce60a9d514a1b062a2b8615309294f71b273b4b7f5b3ce33ef273a36c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:b4c00f3d522ecf35085669952a1e7f8d3bc653c6db8d2ea06745067b7451608b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249278501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7774313fed89667efbcb292dcce4d79ad5a6e1e9fed4140ab8d8047e00642274`
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
# Sat, 28 Oct 2023 03:50:54 GMT
ENV PSMDB_VERSION=5.0.18-15
# Sat, 28 Oct 2023 03:50:54 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:50:54 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Sat, 28 Oct 2023 03:50:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:50:54 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:51:44 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:51:45 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:51:45 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:51:46 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:51:46 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:51:49 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:51:51 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:51:51 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:51:51 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Oct 2023 03:51:51 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:51:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:51:52 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:51:52 GMT
USER 1001
# Sat, 28 Oct 2023 03:51:52 GMT
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
	-	`sha256:a605fb25d797064c47be29eb769c24e001d08f5e8d62528c9efe7f6975e29c27`  
		Last Modified: Sat, 28 Oct 2023 03:56:27 GMT  
		Size: 148.4 MB (148399588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a305dd732c771b772af1d8feba857aec9a57bad33c4ce270ffb377dc4d3504e`  
		Last Modified: Sat, 28 Oct 2023 03:56:09 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69281d35c29eed55833ecda073b13929c3a92e8d007e1370a0faba21cd47cf1d`  
		Last Modified: Sat, 28 Oct 2023 03:56:09 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3551e736d7af41dbfeec0530680cf7b2e5185f5845923953e3c863b0cd79a3`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e72c7531ba87c5ea617cb23b9946f906bced95f2510f026e9edbad8dccd870`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c63c870a7cbb46ad13009b82a0f0aa0c3900d67fbf83d371a5e042d06b341a`  
		Last Modified: Sat, 28 Oct 2023 03:56:08 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00a7f96c3e7582bdc61a7da1ce2c4e0dd2677aae82ba0d162e76974c5846d1f`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b77d413ae8139f271405d0a5d3c3baeccf0cb4d1d28ea2642e7d638ae87dd1`  
		Last Modified: Sat, 28 Oct 2023 03:56:07 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
