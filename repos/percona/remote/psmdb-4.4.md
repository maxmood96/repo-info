## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:327fe0308cc433ac073c80fb7f2f5f0a43a2f27d2c3382bb63bba939d6d14826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:451e6b4e07cf6d749763f47a65b702cfdcb17f6c2336541de205939304ff1a5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195467154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462c5f755710856e73bdb57ea68f7cbef337ce7ff065461baaa08fffe9b64eb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:16 GMT
ADD file:f0e6a328565074e88f761104e323c9f82d10f3a6835f494f792b9550d6c0780c in / 
# Tue, 14 Jun 2022 18:23:17 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:54:39 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 14 Jun 2022 18:57:21 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Tue, 14 Jun 2022 18:57:21 GMT
ENV PSMDB_VERSION=4.4.14-14
# Tue, 14 Jun 2022 18:57:21 GMT
ENV OS_VER=el8
# Tue, 14 Jun 2022 18:57:21 GMT
ENV FULL_PERCONA_VERSION=4.4.14-14.el8
# Tue, 14 Jun 2022 18:57:21 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 14 Jun 2022 18:58:01 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 14 Jun 2022 18:58:02 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 14 Jun 2022 18:58:02 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 14 Jun 2022 18:58:02 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 14 Jun 2022 18:58:03 GMT
ENV GOSU_VERSION=1.11
# Tue, 14 Jun 2022 18:58:05 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 14 Jun 2022 18:58:06 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 14 Jun 2022 18:58:07 GMT
VOLUME [/data/db]
# Tue, 14 Jun 2022 18:58:07 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 14 Jun 2022 18:58:07 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Tue, 14 Jun 2022 18:58:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jun 2022 18:58:08 GMT
EXPOSE 27017
# Tue, 14 Jun 2022 18:58:08 GMT
USER 1001
# Tue, 14 Jun 2022 18:58:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f658974cd1e22c258b47ec713e6cfe60d8f00ec42264206a49a37bf7193cb96e`  
		Last Modified: Tue, 14 Jun 2022 18:24:03 GMT  
		Size: 84.6 MB (84562622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1f3db4f21357a24cefa2a95aee395a71c59b5b9d645a26ea0e5978d9823f89`  
		Last Modified: Tue, 14 Jun 2022 19:01:13 GMT  
		Size: 3.7 MB (3738857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b6bec566b8e441ce66858cdedc1d9c946396d17aeb78b36e9ad94bb511d583`  
		Last Modified: Tue, 14 Jun 2022 19:01:24 GMT  
		Size: 98.1 MB (98079633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b541259522163238f722bda881900bea393de92c9cc9c0b87e26b668dfd648e`  
		Last Modified: Tue, 14 Jun 2022 19:01:12 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e863fed0ec56dd37e684cf7f947183c2cd3f72ce1946bbada511716db5d420`  
		Last Modified: Tue, 14 Jun 2022 19:01:11 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2453b424b1c5e614639121e9a720619118702442ba4a4067c1901cb4d30963`  
		Last Modified: Tue, 14 Jun 2022 19:01:09 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744d3d557c07e413eed5fe2586e65bc9b44cdbdeaeff1b69916d16a10adb0d9e`  
		Last Modified: Tue, 14 Jun 2022 19:01:10 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072ca3034e7e701ab601d7e9ff6346970aa2a656d7726c3c95ae3dc3a514720e`  
		Last Modified: Tue, 14 Jun 2022 19:01:11 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8b8ff213121c7083197ae2a5b4ef92961aa58103b14b971217cfeb5f3a9fbf`  
		Last Modified: Tue, 14 Jun 2022 19:01:09 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07b974d72328cb7c4a90dac5998010d3ba6b9fcbdfb0c2ee1efe32c3067aa43`  
		Last Modified: Tue, 14 Jun 2022 19:01:09 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
