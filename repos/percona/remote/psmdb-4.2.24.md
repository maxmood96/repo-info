## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:eae40ace3716c7b4c7b21095c49064a2c2eb1e5c90843a0cd3379cc979bb786d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:a30af127eca3f6a1cf4fe91ad4942be4d69f0310593f52e367d8f544ef2a461d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231936487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621b1d49929319e71c1fdeb403b36fbf6ce3abd590c50b8941d9c018f5a6873c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:23:03 GMT
ENV PSMDB_VERSION=4.2.24-24
# Wed, 20 Dec 2023 23:23:03 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:23:03 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Wed, 20 Dec 2023 23:23:03 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 20 Dec 2023 23:23:03 GMT
ENV PSMDB_REPO=release
# Wed, 20 Dec 2023 23:23:06 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Wed, 20 Dec 2023 23:23:59 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 20 Dec 2023 23:24:00 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Wed, 20 Dec 2023 23:24:00 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 20 Dec 2023 23:24:01 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 20 Dec 2023 23:24:01 GMT
ENV GOSU_VERSION=1.11
# Wed, 20 Dec 2023 23:24:04 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 20 Dec 2023 23:24:07 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 20 Dec 2023 23:24:07 GMT
VOLUME [/data/db]
# Wed, 20 Dec 2023 23:24:07 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Wed, 20 Dec 2023 23:24:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 23:24:07 GMT
EXPOSE 27017
# Wed, 20 Dec 2023 23:24:07 GMT
USER 1001
# Wed, 20 Dec 2023 23:24:07 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcb1e55dc12491ee0b44a4746c329a2dfdd5ff230fa0f103a5d70761523baa0`  
		Last Modified: Wed, 20 Dec 2023 23:26:56 GMT  
		Size: 4.3 MB (4293774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5e769ea5f5fe1fb3f98563d8011e204206a4e4beb0796b1ca7a78f2c6fce54`  
		Last Modified: Wed, 20 Dec 2023 23:27:10 GMT  
		Size: 117.8 MB (117771177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25297c703b81d2e7c57f81a7e8a5e07588da10eaf7aff59fb3666f8eaf0d0f3a`  
		Last Modified: Wed, 20 Dec 2023 23:26:55 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073ee793ba235bff7e41225e6f5d4718f69a950d37e272a03b992aa4ee1a674d`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e48935a1d0a6c83744fc37653baf566c4bda529b2492842a44c7fa4e23635`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 10.6 KB (10572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a616cb9f129916b2c87a76cd7d48770104314144d803d5bc01bf1a8a1f6fa0bd`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044c09aa9fa7c310857a378cfbdf3481d8dfc1da5431a6970f509799104ddc26`  
		Last Modified: Wed, 20 Dec 2023 23:26:54 GMT  
		Size: 8.2 MB (8151463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c800b094dfb4b1465623575baba8552389da2e259d577313640252401589974f`  
		Last Modified: Wed, 20 Dec 2023 23:26:53 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
