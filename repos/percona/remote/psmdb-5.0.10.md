## `percona:psmdb-5.0.10`

```console
$ docker pull percona@sha256:4e7944ef19d0fa510ba177e54cec7b966d750981876028a7f6540654995b4c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.10` - linux; amd64

```console
$ docker pull percona@sha256:11516aee646ecd52959be96dfd9913d105b29f37face342f5d108049c08809e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213570586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f346ece864c0d4ea6a28454e7428820d0fd59c1265fb63e3fe3a49f64ffcb7fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:02 GMT
ADD file:6e8b447e6b9fb44da452809a15105670b9f9699de7b891279644df73840fdbc5 in / 
# Fri, 27 Jan 2023 23:36:03 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:09:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 28 Jan 2023 00:10:59 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Sat, 28 Jan 2023 00:10:59 GMT
ENV PSMDB_VERSION=5.0.10-9
# Sat, 28 Jan 2023 00:10:59 GMT
ENV OS_VER=el8
# Sat, 28 Jan 2023 00:11:00 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Sat, 28 Jan 2023 00:11:00 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 28 Jan 2023 00:11:40 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 28 Jan 2023 00:11:41 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Sat, 28 Jan 2023 00:11:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 28 Jan 2023 00:11:42 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 28 Jan 2023 00:11:42 GMT
ENV GOSU_VERSION=1.11
# Sat, 28 Jan 2023 00:11:46 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 28 Jan 2023 00:11:50 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 28 Jan 2023 00:11:50 GMT
VOLUME [/data/db]
# Sat, 28 Jan 2023 00:11:51 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Sat, 28 Jan 2023 00:11:51 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Sat, 28 Jan 2023 00:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Jan 2023 00:11:52 GMT
EXPOSE 27017
# Sat, 28 Jan 2023 00:11:52 GMT
USER 1001
# Sat, 28 Jan 2023 00:11:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:cb5daa5c9242ca98c8c9f4eb3fb173f7c14b869619db2cb0de5316725ee9b63c`  
		Last Modified: Fri, 27 Jan 2023 23:37:36 GMT  
		Size: 88.4 MB (88425154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940c732d0c7a0cde19f4efe36b078cc468df1b52af5c82aab9ec1638ec1c35c7`  
		Last Modified: Sat, 28 Jan 2023 00:15:17 GMT  
		Size: 3.8 MB (3771991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b199e1b29aeffb46a03a88791e7a63681f6bf4639943add91a325c6504aab87c`  
		Last Modified: Sat, 28 Jan 2023 00:15:30 GMT  
		Size: 112.3 MB (112287392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27703dae1280f315f6d658a1b75aa9e1cea332e7bfa5409dde0073b55cf654cb`  
		Last Modified: Sat, 28 Jan 2023 00:15:16 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9868352c89c9c8f1724f31a561ef447a4b3eafb18d5849c383c117d3c92aa94`  
		Last Modified: Sat, 28 Jan 2023 00:15:16 GMT  
		Size: 4.1 KB (4098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a928f1bef66985e22b13246964646ada3a66ef85cb56712e1201c02ad42dc66`  
		Last Modified: Sat, 28 Jan 2023 00:15:14 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2621647407be8fe5c2582358c79ecfa949812a9ee6048ef869c3746d3f0e437a`  
		Last Modified: Sat, 28 Jan 2023 00:15:14 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633d781fb664ec088456849a8dd45f05c885d4b084d94d9be1e7a845b393978a`  
		Last Modified: Sat, 28 Jan 2023 00:15:15 GMT  
		Size: 8.1 MB (8137897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca1b8ebf085a503eb0d0111ede5e7ff6c8d0758c31d6c967921e10eb8f234ed`  
		Last Modified: Sat, 28 Jan 2023 00:15:14 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2d4fa7beb15baa59a71fb77c93fdb17de8d1291306a6a40f620beb081df47c`  
		Last Modified: Sat, 28 Jan 2023 00:15:14 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
