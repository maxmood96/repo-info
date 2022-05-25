## `percona:psmdb-4.4.14`

```console
$ docker pull percona@sha256:968e32ae3e4a21e7e32196f636d83a295abc8294801f08dd3f6d575b1ba347bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.14` - linux; amd64

```console
$ docker pull percona@sha256:d8c1173c411cb8e4127b6851b43987f3bbb2993d5132f82c700cf78bdd07509d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195492190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5694b1e7d255a82e8087fea3043d070beb1107b8d70be63c112ca2ae433cd8da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 May 2022 22:41:30 GMT
ADD file:eafd9e49bc2d45c1c5bf5571be43743e0500886224b81c0a07dc7c3d1702d7bb in / 
# Tue, 17 May 2022 22:41:30 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:13:01 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 May 2022 23:15:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 25 May 2022 18:42:12 GMT
ENV PSMDB_VERSION=4.4.14-14
# Wed, 25 May 2022 18:42:12 GMT
ENV OS_VER=el8
# Wed, 25 May 2022 18:42:12 GMT
ENV FULL_PERCONA_VERSION=4.4.14-14.el8
# Wed, 25 May 2022 18:42:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 25 May 2022 18:42:54 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 25 May 2022 18:42:55 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 25 May 2022 18:42:55 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 25 May 2022 18:42:55 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 25 May 2022 18:42:55 GMT
ENV GOSU_VERSION=1.11
# Wed, 25 May 2022 18:42:59 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 25 May 2022 18:43:03 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 25 May 2022 18:43:03 GMT
VOLUME [/data/db]
# Wed, 25 May 2022 18:43:03 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 25 May 2022 18:43:03 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 25 May 2022 18:43:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 May 2022 18:43:04 GMT
EXPOSE 27017
# Wed, 25 May 2022 18:43:04 GMT
USER 1001
# Wed, 25 May 2022 18:43:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:25cd53f41add30fe2e87a488316e4bcfbecf123077c0f9f29be5cd359cbafd32`  
		Last Modified: Tue, 17 May 2022 22:42:23 GMT  
		Size: 84.6 MB (84569034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ff356bca7e3699843c422b64d36df3c5db896eaf92983e8a442cb24e3b3c4`  
		Last Modified: Tue, 17 May 2022 23:19:46 GMT  
		Size: 3.7 MB (3745460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3768a644f40d0e6191df3bd2ea0d9f0d76c5306a9981ef0ce52a7ea32988d2cd`  
		Last Modified: Wed, 25 May 2022 18:44:14 GMT  
		Size: 98.1 MB (98091645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287d34fbe0251993c7912972bba49e60545217f4702568fda9a1966c3af6cbf`  
		Last Modified: Wed, 25 May 2022 18:44:01 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc77ee960fa8eae91d08bc97d83c3b6cd1f49c5c7cd2b22efb1f5abbd536955`  
		Last Modified: Wed, 25 May 2022 18:44:01 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0876f810c6651755997b18e344f4ce75260b019f5196054dd68581f2a1bba69`  
		Last Modified: Wed, 25 May 2022 18:43:59 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a17f451f262e5d1542661bf69a68b4891d9bdd556ba6b8e679b49152835abf2`  
		Last Modified: Wed, 25 May 2022 18:43:59 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da85622fc873c30ab06604cfc94154d2c25c2d8fe12370937ce39cda7334203`  
		Last Modified: Wed, 25 May 2022 18:44:00 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887b792c878a2cd72750f056c5f77b7de119a8f5d55ab61b83ce55252c83f665`  
		Last Modified: Wed, 25 May 2022 18:43:59 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af4f4e262b376380fe4ea8b29673ed9a7d1f881224d544045429b4af47ad220`  
		Last Modified: Wed, 25 May 2022 18:43:59 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
