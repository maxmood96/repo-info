## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:787386afd5396393b71de21d05146bb999be90b2d562972f451232c9c5458451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:04bd621ade908e3cd454ac84eaf4ccac00dc655604240f3bb791b9a8bf0408f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237643918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4988479b39ddc77ad9984dc4c1d5bac4e1cd1df76c08b99ed440e8fbe1ea8ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 21 Sep 2023 23:23:50 GMT
ADD file:f1400f7c015d009a734ef72b857aca20fa0b646827d6d6c0fbd1ec44314f40f1 in / 
# Thu, 21 Sep 2023 23:23:51 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:45:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 21 Sep 2023 23:47:21 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Thu, 21 Sep 2023 23:49:38 GMT
ENV PSMDB_VERSION=4.4.22-21
# Thu, 21 Sep 2023 23:49:38 GMT
ENV OS_VER=el8
# Thu, 21 Sep 2023 23:49:38 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Thu, 21 Sep 2023 23:49:38 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 21 Sep 2023 23:49:38 GMT
ENV PSMDB_REPO=release
# Thu, 21 Sep 2023 23:50:29 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 21 Sep 2023 23:50:30 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 21 Sep 2023 23:50:30 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 21 Sep 2023 23:50:31 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 21 Sep 2023 23:50:31 GMT
ENV GOSU_VERSION=1.11
# Thu, 21 Sep 2023 23:50:33 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 21 Sep 2023 23:50:35 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 21 Sep 2023 23:50:35 GMT
VOLUME [/data/db]
# Thu, 21 Sep 2023 23:50:36 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 21 Sep 2023 23:50:36 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 21 Sep 2023 23:50:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Sep 2023 23:50:36 GMT
EXPOSE 27017
# Thu, 21 Sep 2023 23:50:36 GMT
USER 1001
# Thu, 21 Sep 2023 23:50:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f757f4fc3d201c5d7b9b19e3dbf0ddd78af45972be1834845cecc8fe6a2a5c27`  
		Last Modified: Thu, 21 Sep 2023 23:25:04 GMT  
		Size: 89.0 MB (88977617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4003a78974f8ca57a809c807ac3f02353b39f1aa83d1277ed078d6aa349848`  
		Last Modified: Thu, 21 Sep 2023 23:53:09 GMT  
		Size: 3.8 MB (3793031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c230a61fbf13d310589889e84bed99621d948cb582fe5b1b4e624b5e8840`  
		Last Modified: Thu, 21 Sep 2023 23:54:28 GMT  
		Size: 135.8 MB (135786712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b53d0e8addad3c8c59a46ec4361eef3da6172814cdfb96c00c31a822b19548`  
		Last Modified: Thu, 21 Sep 2023 23:54:10 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc2508062741e16d8e9a4aaf761c12530fadfea638684dcff7eb425797ef38`  
		Last Modified: Thu, 21 Sep 2023 23:54:10 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38ce48d8f598efbeb60afd624f556458d3d1f47e05e799eb52b0ff406307d26`  
		Last Modified: Thu, 21 Sep 2023 23:54:08 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89221d1b69a8e86ff46207dcafea51248d867f6567b7f5a87b32c25b8bf0dfb`  
		Last Modified: Thu, 21 Sep 2023 23:54:08 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61c580064a7b01717619497996882edc03f79376be6c827d056204f09ded6a6`  
		Last Modified: Thu, 21 Sep 2023 23:54:09 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80997276925aa978ed11583a7b268ff50ac143cdec278ec75f45e0502345aaa5`  
		Last Modified: Thu, 21 Sep 2023 23:54:08 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872e665dfa85a94b1918333eda47bba579581c3b471733a7b184eab908ff8d4f`  
		Last Modified: Thu, 21 Sep 2023 23:54:08 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
