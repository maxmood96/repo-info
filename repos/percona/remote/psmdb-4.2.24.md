## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:32d6bd395d9c17bed76c0f30faa337d758544608fb610e5449538bc8701d71cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:d8bb4132f25c09027aca57aaec8d4d9b01a8cdac007b67147b9bf757c620e2a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219064726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137675a39565e1fd389f0c154c1cbdce18ef58efbb379d22f174b4bee5652b88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:48:06 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 11 Aug 2023 01:48:06 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:48:06 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 11 Aug 2023 01:48:07 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:48:07 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:48:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:48:55 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:48:56 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:48:56 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:48:57 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:48:57 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:48:59 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:49:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:49:02 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:49:02 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:49:02 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:49:02 GMT
USER 1001
# Fri, 11 Aug 2023 01:49:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf57b5315533d0ec287f46200a45f69284fdc93e647d9c28be2760714547ae9`  
		Last Modified: Fri, 11 Aug 2023 01:52:39 GMT  
		Size: 3.8 MB (3797086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4951e68cce62765eaba32e9f575f22b69c1489ddf6bf3403921f3d98af263d8`  
		Last Modified: Fri, 11 Aug 2023 01:52:53 GMT  
		Size: 117.3 MB (117258280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5202cacfbc3cf668e909205e857a3b95f74bb5b0780ade9705f761db75d07d4`  
		Last Modified: Fri, 11 Aug 2023 01:52:38 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cc85ba2d940913944c2f44c16f51dc037bcb1991b60b2dcef00ea213b2331a`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee321fffbfeb24e4f4ad6a8c2192f13a623d9ee436c7a3c28c7f098187d15dcd`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09e3d3690e050cb7e46f835d5381f9957bd2226b1f55c5cd4348d03576b5353`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c790b461021fbb20eaa94d3ca96d714c6f52c942b2adccb52c4c2a93f2bf250`  
		Last Modified: Fri, 11 Aug 2023 01:52:38 GMT  
		Size: 8.2 MB (8151460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64ceccb71d3b7f3a22ee4f32d157c1cf568b5cad903fdb46d0742510268ad53`  
		Last Modified: Fri, 11 Aug 2023 01:52:37 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
