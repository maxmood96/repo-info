## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:58e974022f9db146f393f96158fcdcb836dd7da0def4f7bb200b5105cfb752c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:083b66c833f5f8fc6f0545cb41f3a022ea3dfc594eee9d22a9484072b4d7827a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250478152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fe88730a3b801d4007b22353e30426ecb7ce1cf8a6e048f72d559f377747ec`
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
# Thu, 09 May 2024 22:54:02 GMT
ENV PSMDB_VERSION=4.4.22-21
# Thu, 09 May 2024 22:54:02 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:54:02 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Thu, 09 May 2024 22:54:02 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 09 May 2024 22:54:02 GMT
ENV PSMDB_REPO=release
# Thu, 09 May 2024 22:54:57 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 09 May 2024 22:54:59 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Thu, 09 May 2024 22:54:59 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 09 May 2024 22:54:59 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 09 May 2024 22:54:59 GMT
ENV GOSU_VERSION=1.11
# Thu, 09 May 2024 22:55:03 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 09 May 2024 22:55:05 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 09 May 2024 22:55:05 GMT
VOLUME [/data/db]
# Thu, 09 May 2024 22:55:06 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 09 May 2024 22:55:06 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Thu, 09 May 2024 22:55:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 May 2024 22:55:06 GMT
EXPOSE 27017
# Thu, 09 May 2024 22:55:06 GMT
USER 1001
# Thu, 09 May 2024 22:55:06 GMT
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
	-	`sha256:4c82957f5bf3dce34bc5417475d631942a90f102663b0ba8817e504ddf51b6ff`  
		Last Modified: Thu, 09 May 2024 22:59:52 GMT  
		Size: 136.3 MB (136292717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7016c000e84294a551da31987b817606cb5f842270211d476050247e0daba9`  
		Last Modified: Thu, 09 May 2024 22:59:35 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90797bb93bf59f01c0639d3fd340645cb9691af9683a9702dca20e1f51999576`  
		Last Modified: Thu, 09 May 2024 22:59:35 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49fa6f27b0c9be0455889d39273c15a0ffa83fa0b198f35b7dedbf80ee87e05`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77b145c0af7f6c252d5e3680e15463d0ba269dc297413dc71e2362ccb37908`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb52ba09da7b6a9553017e86edcf51e038bf72b799cdc9765f8abac605e379d5`  
		Last Modified: Thu, 09 May 2024 22:59:34 GMT  
		Size: 8.1 MB (8137893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ac9781b18e161913e927fe5a6546829dc3fb0b2a8fa331332778bfb2d79c86`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca3476fe08bc6c190e3fa0d40028966ae476e6dde9698df6c3d6ace841d19ff`  
		Last Modified: Thu, 09 May 2024 22:59:33 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
