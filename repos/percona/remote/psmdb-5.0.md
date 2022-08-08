## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:6a168f91a1e125a4ec5a2ab9a22351b54e47b868c6a12156857a642234d0cf37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:d9ab44fd5b58008b3f86c9c57c02bb63e9e5d669287f4feaa919752fda2534ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209881906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de4d7eabdc62a45bf518d512452688409b199b618e73cfdcc07dc9eba856cf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 08 Aug 2022 19:40:38 GMT
ADD file:583550feec070b3b62d68508a750a70d39b5f2741fbe7e82268da27c0e92f311 in / 
# Mon, 08 Aug 2022 19:40:39 GMT
CMD ["/bin/bash"]
# Mon, 08 Aug 2022 19:43:44 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 08 Aug 2022 19:45:16 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Mon, 08 Aug 2022 19:45:16 GMT
ENV PSMDB_VERSION=5.0.9-8
# Mon, 08 Aug 2022 19:45:16 GMT
ENV OS_VER=el8
# Mon, 08 Aug 2022 19:45:16 GMT
ENV FULL_PERCONA_VERSION=5.0.9-8.el8
# Mon, 08 Aug 2022 19:45:16 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 08 Aug 2022 19:45:55 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Mon, 08 Aug 2022 19:45:56 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Mon, 08 Aug 2022 19:45:56 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Mon, 08 Aug 2022 19:45:57 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Mon, 08 Aug 2022 19:45:57 GMT
ENV GOSU_VERSION=1.11
# Mon, 08 Aug 2022 19:46:00 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Mon, 08 Aug 2022 19:46:16 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Mon, 08 Aug 2022 19:46:17 GMT
VOLUME [/data/db]
# Mon, 08 Aug 2022 19:46:18 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Mon, 08 Aug 2022 19:46:18 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Mon, 08 Aug 2022 19:46:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Aug 2022 19:46:18 GMT
EXPOSE 27017
# Mon, 08 Aug 2022 19:46:18 GMT
USER 1001
# Mon, 08 Aug 2022 19:46:18 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c6c66e8d29aad4dd795924af44e2653db9c88e70d8d5ffc158e799eef5984c4f`  
		Last Modified: Mon, 08 Aug 2022 19:41:30 GMT  
		Size: 84.9 MB (84885626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771004972901639b392e56334f372ad2e4dd7e6e385efaf2a7ca01186c69e1ba`  
		Last Modified: Mon, 08 Aug 2022 19:49:51 GMT  
		Size: 3.8 MB (3757653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d72c76b89385b4cede91a65b8ea495dbe29e8c96f191b56663b6ad12c9354c`  
		Last Modified: Mon, 08 Aug 2022 19:50:05 GMT  
		Size: 112.2 MB (112152574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab560b23a80195694461220b6245c0a843551f7dda4547bd1bb6f71067ed982`  
		Last Modified: Mon, 08 Aug 2022 19:49:50 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98c6963fb68f0d65dfc6d0d5b78a29acb4e9edff7f13c747b041289d4a284d7`  
		Last Modified: Mon, 08 Aug 2022 19:49:50 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117a904fe7abd970ad5601b3c17264f5c1a5d295fd6e969f5efe284f375be5cb`  
		Last Modified: Mon, 08 Aug 2022 19:49:48 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306a433bc8ce269980abab02bef61121ea3b21f4391a2a654091d62e0cdd3c46`  
		Last Modified: Mon, 08 Aug 2022 19:49:48 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3d24b0ae541fbc58b772129b300c272c2a19df902e69bdd43a04f00a443e7`  
		Last Modified: Mon, 08 Aug 2022 19:49:50 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cadad7c3d8d189a82ee13cb835a36eb919091b73f0928890223fec0803c1a7c`  
		Last Modified: Mon, 08 Aug 2022 19:49:48 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddc1c92ab7cd6bc3eb8e5e037c2b70a39354067c4adc3185353a1900b9a3890`  
		Last Modified: Mon, 08 Aug 2022 19:49:48 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
