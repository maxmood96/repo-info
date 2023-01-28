## `percona:psmdb-4.2.21`

```console
$ docker pull percona@sha256:636a8513eb3b02b5d157ddba85d2d4752a7c12e4f8734912a0f75cf46be25609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.21` - linux; amd64

```console
$ docker pull percona@sha256:db8a595f1aa6b43d89895cbc38983972174449f09a1b4c8c7d4847f3bc6d3ba3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178860504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb1cac0528fb33e25a9aca65f58c135cf7d8c02cec7fead88275a67fd865ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:02 GMT
ADD file:6e8b447e6b9fb44da452809a15105670b9f9699de7b891279644df73840fdbc5 in / 
# Fri, 27 Jan 2023 23:36:03 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:09:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Jan 2023 00:12:52 GMT
ENV PSMDB_VERSION=4.2.21-21
# Sat, 28 Jan 2023 00:12:52 GMT
ENV OS_VER=el8
# Sat, 28 Jan 2023 00:12:53 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Sat, 28 Jan 2023 00:12:53 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Jan 2023 00:12:55 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Sat, 28 Jan 2023 00:13:32 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Jan 2023 00:13:33 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Sat, 28 Jan 2023 00:13:33 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Jan 2023 00:13:34 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Jan 2023 00:13:34 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Jan 2023 00:13:36 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Jan 2023 00:13:38 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Jan 2023 00:13:38 GMT
VOLUME [/data/db]
# Sat, 28 Jan 2023 00:13:38 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 28 Jan 2023 00:13:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Jan 2023 00:13:38 GMT
EXPOSE 27017
# Sat, 28 Jan 2023 00:13:38 GMT
USER 1001
# Sat, 28 Jan 2023 00:13:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:cb5daa5c9242ca98c8c9f4eb3fb173f7c14b869619db2cb0de5316725ee9b63c`  
		Last Modified: Fri, 27 Jan 2023 23:37:36 GMT  
		Size: 88.4 MB (88425154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76570414957e666151cfa20070a00c3dc64803b17b991a2e444bce864503ee52`  
		Last Modified: Sat, 28 Jan 2023 00:16:04 GMT  
		Size: 3.8 MB (3771992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bdd3962c254fde863b88b4bf5f470b30c537895ca06cafc702d634a381498e`  
		Last Modified: Sat, 28 Jan 2023 00:16:12 GMT  
		Size: 77.6 MB (77590523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d92c2760abf3d4c1706a49bf343b61891df5e16c57cbafce688e683aa27c53`  
		Last Modified: Sat, 28 Jan 2023 00:16:03 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654da9c365fefae943ec10f48875cefe5cbcf0c2014c2075cefa8e5e83012840`  
		Last Modified: Sat, 28 Jan 2023 00:16:01 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f823dd707abd558c4407e44eabe0054b49b054a75ae250efcd2389627d4e7b5`  
		Last Modified: Sat, 28 Jan 2023 00:16:01 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d01650ef5d4472b2141197054f6d52464eba6222f99d7e6b8ba588938fc7ab8`  
		Last Modified: Sat, 28 Jan 2023 00:16:01 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2fb8df811c974b723ee88a6953b2df37733cf7d3eac651b82a2ac407f747fb`  
		Last Modified: Sat, 28 Jan 2023 00:16:03 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8346674ca462381876853840df7ed9b0170435ab3ccf18bf4022e053fa17a51a`  
		Last Modified: Sat, 28 Jan 2023 00:16:01 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
