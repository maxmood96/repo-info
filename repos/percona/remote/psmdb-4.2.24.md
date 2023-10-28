## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:74761747d355301a1d38fa59a0c29c31087a0973725114bc05fb6cd4aef4c3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:740a210c719ab774d451ff24d1fec8836a54b83f7e2c7c617a04f706b0058f96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218126011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723d220fe3f8870c53d88843c03d7b858917fc6e3861af6added68494279a0cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 28 Oct 2023 00:43:16 GMT
ADD file:71adc1eef3a45dd9caba00e0f21cb1c3fcce14492658a0164858a6bff23246a8 in / 
# Sat, 28 Oct 2023 00:43:17 GMT
CMD ["/bin/bash"]
# Sat, 28 Oct 2023 03:48:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Oct 2023 03:53:14 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 28 Oct 2023 03:53:14 GMT
ENV OS_VER=el8
# Sat, 28 Oct 2023 03:53:14 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 28 Oct 2023 03:53:14 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Oct 2023 03:53:14 GMT
ENV PSMDB_REPO=release
# Sat, 28 Oct 2023 03:53:17 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 28 Oct 2023 03:54:04 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Oct 2023 03:54:05 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 28 Oct 2023 03:54:05 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Oct 2023 03:54:06 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Oct 2023 03:54:06 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Oct 2023 03:54:09 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Oct 2023 03:54:11 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Oct 2023 03:54:11 GMT
VOLUME [/data/db]
# Sat, 28 Oct 2023 03:54:11 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 28 Oct 2023 03:54:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Oct 2023 03:54:11 GMT
EXPOSE 27017
# Sat, 28 Oct 2023 03:54:11 GMT
USER 1001
# Sat, 28 Oct 2023 03:54:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:90b8c6487b7adc2185a51b6afb1254caf4e0b0ef45a33c47240e1dba2afd6a42`  
		Last Modified: Sat, 28 Oct 2023 00:44:09 GMT  
		Size: 88.0 MB (88004859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ea63e2471396fb3eafc4042ce991f96da511443b418212d7ad8c326199d2cf`  
		Last Modified: Sat, 28 Oct 2023 03:57:06 GMT  
		Size: 3.8 MB (3787465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51032f70d0821cf41c15684232cf756663ba7288db50655496bd03b85acc342e`  
		Last Modified: Sat, 28 Oct 2023 03:57:20 GMT  
		Size: 117.2 MB (117246763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b405104fc2a9b3b3fa936bba18ef021014e9348dd8c70c66e9fb6762513baca`  
		Last Modified: Sat, 28 Oct 2023 03:57:06 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d8db8dc48968264c1516d3ec031d58aa1b262d27a4e1e16cf15a59305e143`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a48b2ee810ca3fbbf924e3928b3a687e6db5fb25126c3af1b8a17a5343b410`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed26e5f822fc5e75c7b5dccfb2771db943f353d591fd54227450376f9c181abb`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2839ab117c76045e458ccfcc12efa69ead2c9bc8836d58de960187104c85181`  
		Last Modified: Sat, 28 Oct 2023 03:57:05 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0810186cf8a50eebd3483cb237f80250d90c3be190db708b94136cc2bff06c60`  
		Last Modified: Sat, 28 Oct 2023 03:57:04 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
