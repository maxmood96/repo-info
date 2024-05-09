## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:f641c2d3628038fb33a89986376790ab9fb95f84f81c54ac61c726c5befaf9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:b0010065796bf22a39650185d5147047e3e5834bc502cacb3b98a98c24404366
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263081395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706626b126c5ac852e69f15fcaed42052462300520072d73995d72c9aa5bfd38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:51:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 09 May 2024 22:52:52 GMT
ENV PSMDB_VERSION=5.0.18-15
# Thu, 09 May 2024 22:52:52 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:52:52 GMT
ENV FULL_PERCONA_VERSION=5.0.18-15.el8
# Thu, 09 May 2024 22:52:52 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:52:52 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:53:48 GMT
RUN set -ex;     percona-release enable psmdb-50 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:53:50 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:53:50 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:53:50 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:53:50 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:53:53 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:53:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:53:55 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:53:56 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:53:56 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Thu, 09 May 2024 22:53:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:53:56 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:53:56 GMT
USER 1001
# Thu, 09 May 2024 22:53:57 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74628cc9f6fe7927ea24cc394193c7bd60fa9a6d344603584dadfb4b2f5722a`  
		Last Modified: Thu, 09 May 2024 22:58:36 GMT  
		Size: 4.3 MB (4297822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211782ad7d02bd0eeee8cf9091490ca4f1d54205f32a95ce11f2bcf07f6b64f`  
		Last Modified: Thu, 09 May 2024 22:59:24 GMT  
		Size: 148.9 MB (148895973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f835a8bc63440967b9cb11598ff2cc53653d0b792385c4bc00cb0abd24fbddfd`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727aea791b52fbb3fef4ee0fcfef4c9cd446278ab7ed0893aec30e882f11ccd4`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 4.1 KB (4101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5177a5fe558b8b0510657aa7aff0f63b994a807103c2b8c8ff830bcdce14c314`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d1a14cf48c9cf9d2811791256b547d194e4464e7df8b437a442c784f073883`  
		Last Modified: Thu, 09 May 2024 22:59:05 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb257e3773ad4746dd279d5e968c36b0b14158d57c43f25875e56255317408`  
		Last Modified: Thu, 09 May 2024 22:59:06 GMT  
		Size: 8.1 MB (8137886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ead6839765afb0c5e7cabcad29242c6fa190e6856b0d7042a3472b3090009d6`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963fdd9a787aa0a5d128a2e88246c7fb5ab158b65abf1fd859d5a39eec5d146f`  
		Last Modified: Thu, 09 May 2024 22:59:04 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
