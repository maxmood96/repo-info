## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:1b1b46312aaba0e59d27005865791a70519a7ce82a899e8ed83c94cd80cf6548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:7e77cc24bad18a0bf4f4ff4420a96d5c79f862dac5bba37416f7252a9c515f60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195531113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6f4dab2f467e62c0b9bf2bd1675d042ba38b8dd27b9526910bc939c959b479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:24 GMT
ADD file:05afe15e1c394de999f38bb2413c80af18f129511261f53511fe21e4606b6353 in / 
# Tue, 05 Jul 2022 22:20:24 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:42:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 05 Jul 2022 22:44:32 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Wed, 20 Jul 2022 18:20:11 GMT
ENV PSMDB_VERSION=4.4.15-15
# Wed, 20 Jul 2022 18:20:11 GMT
ENV OS_VER=el8
# Wed, 20 Jul 2022 18:20:11 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Wed, 20 Jul 2022 18:20:11 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Jul 2022 18:20:49 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Jul 2022 18:20:50 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 20 Jul 2022 18:20:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Jul 2022 18:20:51 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Jul 2022 18:20:51 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Jul 2022 18:20:55 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Jul 2022 18:20:59 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Jul 2022 18:20:59 GMT
VOLUME [/data/db]
# Wed, 20 Jul 2022 18:21:00 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 20 Jul 2022 18:21:00 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Wed, 20 Jul 2022 18:21:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 18:21:00 GMT
EXPOSE 27017
# Wed, 20 Jul 2022 18:21:00 GMT
USER 1001
# Wed, 20 Jul 2022 18:21:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:15a6facc77411902de6b8de2d42125695286cd602d17db01f09239a7f6f8992a`  
		Last Modified: Tue, 05 Jul 2022 22:21:25 GMT  
		Size: 84.6 MB (84566504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087a8e4f03adb98187b969d21754834825844141948311fad71ba7367cfd7ab2`  
		Last Modified: Tue, 05 Jul 2022 22:48:16 GMT  
		Size: 3.7 MB (3734428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a69217730608110b45cbcc1b2c0c69ef99112b5fc790598fd8e5617597b97c`  
		Last Modified: Wed, 20 Jul 2022 18:22:16 GMT  
		Size: 98.1 MB (98144127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1231380a664963d555ef1e3e717c9e07625516526986fdf4d136257b4b88eeb`  
		Last Modified: Wed, 20 Jul 2022 18:22:03 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f180e3af77b942937b87071d178ed7331f724479340a12246638c86f1fac1e`  
		Last Modified: Wed, 20 Jul 2022 18:22:03 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a875e9c8fd4be5a2505c40a3e79afdd5d8f3060977dfd82e118e59da7c3d1`  
		Last Modified: Wed, 20 Jul 2022 18:22:01 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0c36f7c7d3ecc4fdb284040cab9ce547c280cc94c490df52a93a48f81d7a8`  
		Last Modified: Wed, 20 Jul 2022 18:22:01 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41745bf039071ea2b0d1686e9a7d918292ed2543f7b4ec355a3288ad98e1bfc`  
		Last Modified: Wed, 20 Jul 2022 18:22:02 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd61b29354a341eadf3cc15b1c78c96e02a103c600c46fe63e7773bfeb8c872`  
		Last Modified: Wed, 20 Jul 2022 18:22:01 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4598af39cb8837b1f59cad0f911a54c6b3bf37206d0aafbb9ccfea21b38318b`  
		Last Modified: Wed, 20 Jul 2022 18:22:01 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
