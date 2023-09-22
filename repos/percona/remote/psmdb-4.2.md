## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:414fba4f2cb6393e6732288c7e996d6528acb4de8852b7e74be571bce8acc1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:c9df0a237c305485f633d662a5ce1041b4b09dcfc679f19617feddb857fdbaf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219114361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565f9b7c885acc4fbf3a5b0fcbc839fef15d4a057fb52551a876381314c91fac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 21 Sep 2023 23:23:50 GMT
ADD file:f1400f7c015d009a734ef72b857aca20fa0b646827d6d6c0fbd1ec44314f40f1 in / 
# Thu, 21 Sep 2023 23:23:51 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:45:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 21 Sep 2023 23:50:48 GMT
ENV PSMDB_VERSION=4.2.24-24
# Thu, 21 Sep 2023 23:50:48 GMT
ENV OS_VER=el8
# Thu, 21 Sep 2023 23:50:48 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Thu, 21 Sep 2023 23:50:48 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 21 Sep 2023 23:50:49 GMT
ENV PSMDB_REPO=release
# Thu, 21 Sep 2023 23:50:51 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 21 Sep 2023 23:51:40 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 21 Sep 2023 23:51:41 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 21 Sep 2023 23:51:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 21 Sep 2023 23:51:42 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 21 Sep 2023 23:51:42 GMT
ENV GOSU_VERSION=1.11
# Thu, 21 Sep 2023 23:51:45 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 21 Sep 2023 23:51:47 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 21 Sep 2023 23:51:47 GMT
VOLUME [/data/db]
# Thu, 21 Sep 2023 23:51:48 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Thu, 21 Sep 2023 23:51:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Sep 2023 23:51:48 GMT
EXPOSE 27017
# Thu, 21 Sep 2023 23:51:48 GMT
USER 1001
# Thu, 21 Sep 2023 23:51:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f757f4fc3d201c5d7b9b19e3dbf0ddd78af45972be1834845cecc8fe6a2a5c27`  
		Last Modified: Thu, 21 Sep 2023 23:25:04 GMT  
		Size: 89.0 MB (88977617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807209c0683a4d5f3ba520355288f8af21bb206567626fddbe3059fbc831d20e`  
		Last Modified: Thu, 21 Sep 2023 23:54:40 GMT  
		Size: 3.8 MB (3793090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f0a6ae3bd8753285a3ef752362337683573121676111e290af279bde42f87`  
		Last Modified: Thu, 21 Sep 2023 23:54:54 GMT  
		Size: 117.3 MB (117256737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36192c58d3c3806843c72df51f68099517e15c520214296cc7de63e9f7bfc4af`  
		Last Modified: Thu, 21 Sep 2023 23:54:39 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3318d86d153c93a4441f8af8699a623000a53a88915643f08b0b33138098872f`  
		Last Modified: Thu, 21 Sep 2023 23:54:38 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffdc9576a6a3c0442de100c2d3ca0249d2bde5ca1377a770df88c7629831939`  
		Last Modified: Thu, 21 Sep 2023 23:54:38 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848f329f2e34276a857f96e6b22fcb83da4102a89508544dec9dfd3d7be73ec2`  
		Last Modified: Thu, 21 Sep 2023 23:54:38 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d89db9d8185c68da5475ecb944a2001ff62d7cb6ad3c5d69b97d1ae2dd0477`  
		Last Modified: Thu, 21 Sep 2023 23:54:40 GMT  
		Size: 8.2 MB (8151455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148f378ef29898a3a3b6ff7eec618a4957efe5ada1d448ea6cc18a40f075b7f2`  
		Last Modified: Thu, 21 Sep 2023 23:54:38 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
