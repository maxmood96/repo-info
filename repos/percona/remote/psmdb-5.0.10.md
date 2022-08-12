## `percona:psmdb-5.0.10`

```console
$ docker pull percona@sha256:d8c7a30a55ea2b4bdf6283a9006c6a9bda7c9b8c4683478803cf7d46781f8b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.10` - linux; amd64

```console
$ docker pull percona@sha256:29b9ab88c365b8ff5aa2b60c55048599ea394efe9dd2309e10e8d0a316041485
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210020023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d394a9ce1c68c983eb78344580b62a19475740771a765754ba8816e7717390be`
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
# Fri, 12 Aug 2022 21:05:09 GMT
ENV PSMDB_VERSION=5.0.10-9
# Fri, 12 Aug 2022 21:05:09 GMT
ENV OS_VER=el8
# Fri, 12 Aug 2022 21:05:09 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Fri, 12 Aug 2022 21:05:09 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 12 Aug 2022 21:05:49 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 12 Aug 2022 21:05:50 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 12 Aug 2022 21:05:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 12 Aug 2022 21:05:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 12 Aug 2022 21:05:50 GMT
ENV GOSU_VERSION=1.11
# Fri, 12 Aug 2022 21:05:54 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 12 Aug 2022 21:05:57 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 12 Aug 2022 21:05:57 GMT
VOLUME [/data/db]
# Fri, 12 Aug 2022 21:05:58 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 12 Aug 2022 21:05:58 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 12 Aug 2022 21:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Aug 2022 21:05:58 GMT
EXPOSE 27017
# Fri, 12 Aug 2022 21:05:59 GMT
USER 1001
# Fri, 12 Aug 2022 21:05:59 GMT
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
	-	`sha256:4672ac2da6ecc365b0f8fb57516d8128cf2541762549d1928b5a52a60b8c971e`  
		Last Modified: Fri, 12 Aug 2022 21:07:15 GMT  
		Size: 112.3 MB (112290685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb59e2b7a6bc194242561877e0c1a3cbb6a8ac29552a2e579978776d33589cb`  
		Last Modified: Fri, 12 Aug 2022 21:07:00 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeeabc90ae45fb2dff5bf995c006013a83daa4db90ac22c0a488ffa725a5b2cb`  
		Last Modified: Fri, 12 Aug 2022 21:07:00 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32264cb786a04d9bb4425fda94dd0b8d6c9cd8f43f4e3ab58d485c08e904e50f`  
		Last Modified: Fri, 12 Aug 2022 21:06:58 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d70fcc8d22639d46adfe63f135d2c5be4d780fe0d9ded2e2f6de8345c03af8`  
		Last Modified: Fri, 12 Aug 2022 21:06:58 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13602a7ad5bc43b6ec1193ca0cb59913e30344a490507828d3f89d55190bcd2`  
		Last Modified: Fri, 12 Aug 2022 21:06:59 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087629b5052ff13d9f02658ec046f2f8a1e58428a37b3ebfe70b2009dbfa8b7a`  
		Last Modified: Fri, 12 Aug 2022 21:06:58 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e485cfa3b535a5bd6d0c70c8b034dae7164bb57070749b60cb4f5d353a059d`  
		Last Modified: Fri, 12 Aug 2022 21:06:58 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
