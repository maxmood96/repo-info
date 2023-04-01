## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:b84ed6f2349c44fb0a76c66812716f3a17553a61472934fc3beb5a5272b97dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:2178c5fcd7b1fb5f5373495ccf3922e1ddf2aeae9940a9e3c8277b1c2f02b3d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213570843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7a42bcd5ace1b180629bc7b4d65b4e764830f73db1efc2fef4de89c44a6677`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 31 Mar 2023 22:28:30 GMT
ADD file:612f06c9f5ab410219b2415de45592033d4e9a8d5ce398134276a90224363fb7 in / 
# Fri, 31 Mar 2023 22:28:31 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:15:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 31 Mar 2023 23:15:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Fri, 31 Mar 2023 23:15:59 GMT
ENV PSMDB_VERSION=5.0.10-9
# Fri, 31 Mar 2023 23:15:59 GMT
ENV OS_VER=el8
# Fri, 31 Mar 2023 23:15:59 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Fri, 31 Mar 2023 23:15:59 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 31 Mar 2023 23:16:39 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 31 Mar 2023 23:16:40 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 31 Mar 2023 23:16:40 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 31 Mar 2023 23:16:41 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 31 Mar 2023 23:16:41 GMT
ENV GOSU_VERSION=1.11
# Fri, 31 Mar 2023 23:16:45 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 31 Mar 2023 23:16:47 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 31 Mar 2023 23:16:47 GMT
VOLUME [/data/db]
# Fri, 31 Mar 2023 23:16:48 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 31 Mar 2023 23:16:48 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 31 Mar 2023 23:16:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Mar 2023 23:16:48 GMT
EXPOSE 27017
# Fri, 31 Mar 2023 23:16:48 GMT
USER 1001
# Fri, 31 Mar 2023 23:16:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:41733b29f9a8eca496b29d689caae2300f16590d79b84a98ea73605fb00ed04b`  
		Last Modified: Fri, 31 Mar 2023 22:29:52 GMT  
		Size: 88.4 MB (88437312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e800ad102f61744378b09a4af7e450c34894e0d455d276e64229aa4419de8af9`  
		Last Modified: Fri, 31 Mar 2023 23:19:59 GMT  
		Size: 3.8 MB (3764057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b50c34e26b543fc53404cbb78d5032cbb17115897b0e03a4e956198acf0df50`  
		Last Modified: Fri, 31 Mar 2023 23:20:12 GMT  
		Size: 112.3 MB (112283428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e8bda200ea5511e7c006b9bfe59bc6a8275ac8b4084d306045a4722e5179be`  
		Last Modified: Fri, 31 Mar 2023 23:19:58 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa44fd97d973dc79fee2503508b86eac82f222e1b09ce5cca16b892354c6411`  
		Last Modified: Fri, 31 Mar 2023 23:19:58 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d41c69984c86acde83d4fb2c81667665c5efa710588c29f3479bdb8c63e044e`  
		Last Modified: Fri, 31 Mar 2023 23:19:57 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b680fb3ee989861477e24d6eea4e4ca4051899861cf7b83941b4a1a0c4c68325`  
		Last Modified: Fri, 31 Mar 2023 23:19:57 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb932c975de0d59172d3269c45186ce05a4ef762d2c41e923e1ad1cd1113586`  
		Last Modified: Fri, 31 Mar 2023 23:19:58 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb672caf438d081b19bf59cbdf24e277c570694dc14cb54a88b6535f98d27cc4`  
		Last Modified: Fri, 31 Mar 2023 23:19:57 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aaa111bd79dc4119c5828a27d8b500c1234da7f3056664d9580fb6341b2dc7`  
		Last Modified: Fri, 31 Mar 2023 23:19:57 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
