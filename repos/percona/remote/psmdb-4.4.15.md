## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:6b1e7112d99fdc1bcf0a7e8b4936b52481bd13a654214f7395df813c74227e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:b38edb025de7d4a924167ff73332384e8444d4d82ff7a31235b39726903ea71a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195737024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8408feb59c06bfcf83aa7b23ec2f3ad0608951a4af35b3d865b620e6ab2f2fb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 27 Oct 2022 17:21:34 GMT
ADD file:21d51ed5d75272951d93bd7d363ccf19173ef416b25c6acb627b575293fb7389 in / 
# Thu, 27 Oct 2022 17:21:35 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 17:45:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 27 Oct 2022 17:47:59 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Thu, 27 Oct 2022 17:47:59 GMT
ENV PSMDB_VERSION=4.4.15-15
# Thu, 27 Oct 2022 17:47:59 GMT
ENV OS_VER=el8
# Thu, 27 Oct 2022 17:47:59 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Thu, 27 Oct 2022 17:48:00 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 27 Oct 2022 17:48:37 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 27 Oct 2022 17:48:38 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 27 Oct 2022 17:48:38 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 27 Oct 2022 17:48:39 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 27 Oct 2022 17:48:39 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Oct 2022 17:48:42 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 27 Oct 2022 17:48:44 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 27 Oct 2022 17:48:44 GMT
VOLUME [/data/db]
# Thu, 27 Oct 2022 17:48:45 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 27 Oct 2022 17:48:45 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 27 Oct 2022 17:48:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 17:48:45 GMT
EXPOSE 27017
# Thu, 27 Oct 2022 17:48:45 GMT
USER 1001
# Thu, 27 Oct 2022 17:48:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1ca7c848b9e5e4ce2ec73f5399f2b0c161b4c592c979bfb25cd1acc15ea0d84a`  
		Last Modified: Thu, 27 Oct 2022 17:23:09 GMT  
		Size: 86.0 MB (85963514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d597402d8f660a9aa066e0360ee15528e8fd2254739934a86e3601b0309993f2`  
		Last Modified: Thu, 27 Oct 2022 17:52:04 GMT  
		Size: 3.8 MB (3773725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de158455bf8284227c45b8fcc6bb4feb0079d09f900f0b8233d91ca3450a815`  
		Last Modified: Thu, 27 Oct 2022 17:52:15 GMT  
		Size: 96.9 MB (96913728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c8b071085a02e3d6e799f0322620ac7411657f16ed82bb553c90a7f61791f9`  
		Last Modified: Thu, 27 Oct 2022 17:52:02 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba7709a6853ade1f4add62d891a5d24bde6fe4117e40e90984241c044837353`  
		Last Modified: Thu, 27 Oct 2022 17:52:02 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b5bd493bc393def2a201b0bc8e3f3e16587ebbe28109fe9b78e5368078b73c`  
		Last Modified: Thu, 27 Oct 2022 17:52:00 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c435ea658803a465493f995fe2bead8c28052bf2e611c7bd95641f41e1c7ba`  
		Last Modified: Thu, 27 Oct 2022 17:52:00 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c8e2a20af0d92c489de35593dac6a954bb085cf1593d3d6526a5379eb4e472`  
		Last Modified: Thu, 27 Oct 2022 17:52:02 GMT  
		Size: 8.1 MB (8137894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda8bdf00d77c4b1114283e82fa6a2cc85fb53dcb799889bd3dce78f1bfd9155`  
		Last Modified: Thu, 27 Oct 2022 17:52:00 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037a3ec19357e44c22e62a353271618c064363d93dc00e90811929a892b8630e`  
		Last Modified: Thu, 27 Oct 2022 17:52:00 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
