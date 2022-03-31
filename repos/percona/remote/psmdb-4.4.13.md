## `percona:psmdb-4.4.13`

```console
$ docker pull percona@sha256:52199cc3810fd63cf6067b7abdf76e954f5efdc871be5bf91527851f1f59174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.13` - linux; amd64

```console
$ docker pull percona@sha256:8b4db323f11f94b32a5a1b75066973600e98b3fff4c36fc2e87050d25189dd4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.4 MB (198364787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab653360447173f2e0af2b45dcf27d25a98d24e74e937cfb8044c6032317480a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:33 GMT
ADD file:d94132182c035117e6c34ac6179798583b0adcdb2790160d2740b5a23dfef57b in / 
# Tue, 29 Mar 2022 18:35:34 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:14:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 31 Mar 2022 02:16:01 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Thu, 31 Mar 2022 02:16:01 GMT
ENV PSMDB_VERSION=4.4.13-13
# Thu, 31 Mar 2022 02:16:01 GMT
ENV OS_VER=el8
# Thu, 31 Mar 2022 02:16:01 GMT
ENV FULL_PERCONA_VERSION=4.4.13-13.el8
# Thu, 31 Mar 2022 02:16:01 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 31 Mar 2022 02:16:38 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 31 Mar 2022 02:16:39 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 31 Mar 2022 02:16:39 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 31 Mar 2022 02:16:40 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 31 Mar 2022 02:16:40 GMT
ENV GOSU_VERSION=1.11
# Thu, 31 Mar 2022 02:16:43 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 31 Mar 2022 02:16:46 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 31 Mar 2022 02:16:47 GMT
VOLUME [/data/db]
# Thu, 31 Mar 2022 02:16:47 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 31 Mar 2022 02:16:47 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 31 Mar 2022 02:16:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 31 Mar 2022 02:16:48 GMT
EXPOSE 27017
# Thu, 31 Mar 2022 02:16:48 GMT
USER 1001
# Thu, 31 Mar 2022 02:16:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f194d33a6f3eb80ec1d36f30e468274de9bc57c56876707532a364fe1edb59b7`  
		Last Modified: Tue, 29 Mar 2022 18:36:37 GMT  
		Size: 87.5 MB (87480759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe12f41913d5bb12473c34940d7ec6c197ceafb8851bdbc754d656ca52ec814`  
		Last Modified: Thu, 31 Mar 2022 02:19:23 GMT  
		Size: 3.8 MB (3754362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9537222177d90520db2db7c1c69ac3d83bee1c5c50fc7ceb6c7d3ce78ef1ff`  
		Last Modified: Thu, 31 Mar 2022 02:19:35 GMT  
		Size: 98.0 MB (98043614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b717f70922d3c89e7d0975e10da126f1679a148cbabb237846540a8e9a492afd`  
		Last Modified: Thu, 31 Mar 2022 02:19:22 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f45bfb7e076179bbeb584d8ab88e4f7db0902ba194f12790e99a3bb78994ce`  
		Last Modified: Thu, 31 Mar 2022 02:19:22 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff62910c89421da2063282f281176b8b9f72b522dda08734018d0863c10fd54`  
		Last Modified: Thu, 31 Mar 2022 02:19:20 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114decfc1494ba7e4721d97a3d99988ee4808c8e99ef82ac92e2fc4c59b9967b`  
		Last Modified: Thu, 31 Mar 2022 02:19:20 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5cc7f6387daf3f2819ce9e3330c1fca3e856f50ee30d4624eaba3e8b0e7d5b7`  
		Last Modified: Thu, 31 Mar 2022 02:19:21 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde7f33c5bab1225c2100b241727fd6a73dc1aeda5847745832a23699e01ef9d`  
		Last Modified: Thu, 31 Mar 2022 02:19:20 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35330255ae4c1b172799a41dd434483434f521e8e767581760f2066d22310834`  
		Last Modified: Thu, 31 Mar 2022 02:19:20 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
